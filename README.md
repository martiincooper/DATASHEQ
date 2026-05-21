# Datasheq — UI/UX demo

Vista previa estática de la nueva web de **Datasheq** (plataforma SaaS B2B de cumplimiento
legal, control documental, verificaciones inteligentes y gestión operativa).

> Este proyecto es **solo demo de UI/UX**. No tiene backend, no envía datos a ningún servicio
> y no requiere configuración de secretos. El formulario de contacto muestra un mensaje
> de éxito de forma puramente visual.

## Estructura

```
datasheq/
├── public/                # Sitio estático (todo lo que se publica)
│   ├── index.html         # Landing principal
│   ├── styles.css
│   ├── favicon.svg
│   ├── og-image.svg
│   ├── privacidad.html
│   └── terminos.html
├── wrangler.toml          # Cloudflare Workers Static Assets (solo assets, sin Worker)
└── README.md
```

## Desarrollo local

Cualquier servidor estático sirve. Ejemplos:

```bash
# Opción A — Wrangler (igual al runtime productivo de Cloudflare)
npx wrangler dev

# Opción B — Python
cd public && python3 -m http.server 8080

# Opción C — Node
npx serve public
```

## Deploy en Cloudflare

```bash
npx wrangler deploy
```

Eso es todo. No hay variables de entorno ni secretos que configurar.
