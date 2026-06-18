# agenciaseo.davidviejo.com

Repositorio preparado para publicar documentos HTML estáticos en Vercel bajo el subdominio `agenciaseo.davidviejo.com`.

## Funcionamiento

- La página de inicio (`/`) redirige permanentemente a `https://agenciaseo.eu/`.
- Los documentos se comparten mediante enlaces directos a cada archivo HTML.
- Todo el sitio está configurado como `noindex, nofollow` mediante:
  - Meta robots en cada HTML.
  - Cabecera HTTP `X-Robots-Tag` desde `vercel.json`.
  - `robots.txt` con `Disallow: /`.

## Primer documento disponible

- `economia3 enlazado interno.html`

URL esperada tras conectar el dominio en Vercel:

```text
https://agenciaseo.davidviejo.com/economia3%20enlazado%20interno.html
```

## Añadir nuevos documentos

1. Añade el nuevo archivo `.html` en la raíz del repositorio.
2. Incluye en el `<head>` del HTML:

```html
<meta name="robots" content="noindex, nofollow">
```

3. Haz deploy en Vercel y comparte únicamente la URL directa del archivo.
