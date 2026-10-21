# Firmas de email · Todo Drones / NexGen

Página interna donde cada persona busca su nombre, ve su firma de Gmail y la copia.
Hay tres variantes: **NexGen**, **Todo Drones** (consumer) y **Todo Drones Agro**.

Sitio estático, sin build: `index.html` + `people.json` + `img/`.

## Agregar o modificar personas

Editá `people.json` (desde GitHub mismo) y hacé commit; Vercel lo publica solo.

```json
{
  "nombre": "Nombre Apellido",
  "email": "nombre@tododrones.com.ar",
  "empresa": "consumer",            // "nexgen" | "consumer" | "agro"
  "area": "Comercial",
  "puesto": "Responsable comercial",
  "telefono": "+54 9 11 1234-5678",  // siempre con código de país
  "direccion": "Av Dardo Rocha 2934, Martinez",
  "web": "https://www.tododrones.com.ar/",
  "instagram": "https://www.instagram.com/tododrones.arg",
  "facebook": "https://www.facebook.com/TodoDronesArg",
  "linkedin": ""
}
```

Link directo a la firma de alguien: `https://<dominio>/#<mail con guiones>`,
por ejemplo `#justo-tododrones-com-ar`.

## Imágenes

Los logos e íconos de las firmas se sirven desde `img/` en este mismo sitio, así que el
dominio de producción de Vercel tiene que ser público (las previews con Vercel
Authentication no sirven para copiar firmas). Si cambia el dominio, cada persona tiene que
volver a copiar su firma.

## Deploy en Vercel

New Project → importar `justo-td/firmas` → Framework Preset **Other**, sin build command ni
output directory → Deploy.
