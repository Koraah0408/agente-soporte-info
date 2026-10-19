# Agente de Soporte IA — Páginas informativas

Este repositorio contiene las dos páginas web públicas de la aplicación **Agente de Soporte IA**, publicadas con GitHub Pages. El código del agente está en un repositorio aparte: [`agente_soporte`](https://github.com/Koraah0408/agente_soporte).

## Páginas publicadas

| Página | Archivo | URL |
|---|---|---|
| Página principal | `index.html` | https://koraah0408.github.io/agente-soporte-info/ |
| Política de privacidad | `privacidad.html` | https://koraah0408.github.io/agente-soporte-info/privacidad.html |

## ¿Para qué existen?

Para publicar la aplicación de Google Cloud en modo **En producción**, Google exige que tenga una página principal y una política de privacidad accesibles en internet. En modo *Testing*, el token de acceso a Google caduca a los 7 días y el agente deja de funcionar. Estas páginas permiten que el token sea permanente.

Esas URL se registran en Google Cloud Console, en **Pantalla de consentimiento de OAuth → Desarrollo de la marca**:

- Página principal de la aplicación → `index.html`
- Vínculo a la política de privacidad → `privacidad.html`
- Dominio autorizado → `koraah0408.github.io`

## ¿Qué hace la aplicación?

Agente de Soporte IA revisa las respuestas de un formulario guardadas en Google Sheets, usa Gemini para clasificar cada queja (Ventas, Soporte Técnico o Logística) y detectar su sentimiento (Positivo, Negativo o Neutro), y escribe el resultado en la misma hoja de cálculo.

Es un proyecto escolar del taller de automatización con IA, de uso personal.

## Estructura

```
agente-soporte-info/
├── README.md
├── index.html        <- página principal de la app
└── privacidad.html   <- política de privacidad
```

## Cómo se publica

GitHub Pages sirve el contenido directamente desde la rama `main`, carpeta raíz (`/`):

**Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)`**

Cada cambio que se sube a `main` se publica automáticamente en uno o dos minutos.

## Nota de seguridad

Este repositorio es **público**. Por eso solo contiene las dos páginas HTML: no incluye claves de API, tokens, credenciales ni datos de clientes.

## Contexto del proyecto

| Práctica | Qué se hizo |
|---|---|
| 1 | Agente de soporte en Python (Gemini + Google Forms/Sheets) |
| 2 | Despliegue en la nube con GitHub Actions y publicación de la app de Google en producción (este repo) |
| 3 | Empaquetado del agente en un contenedor con Docker |
