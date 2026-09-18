# De sitio estático a aplicación real

Publicar en GitHub Pages resuelve **el acceso**: el sistema queda en una dirección
web, funciona desde cualquier teléfono y se puede probar sin instalar nada.

No resuelve **los datos compartidos**. Hoy cada navegador guarda su propia copia:
si un médico hace un pedido en su teléfono, ese pedido no aparece en la computadora
de la bodega. Son dos islas.

## Lo que falta para la app del médico

| Pieza | Qué resuelve | Opción sugerida | Costo |
|---|---|---|---|
| Hosting | Que el sistema tenga dirección web | GitHub Pages | Gratis |
| Base de datos compartida | Que el pedido del médico llegue a bodega | Supabase | Gratis hasta ~500 MB |
| Identificación del médico | Que cada quien vea lo suyo | Supabase Auth por teléfono | Incluido |
| Aviso al médico | Alertas de reposición | Notificaciones web (PWA) | Gratis |
| Instalable en el teléfono | Icono en pantalla de inicio, sin tienda de apps | Manifest + service worker | Gratis |

## Secuencia recomendada

1. **Publicar lo actual en GitHub Pages.** Probar desde el teléfono que todo se ve bien.
2. **Convertirlo en PWA** (instalable, funciona sin señal). Cambio menor sobre lo existente.
3. **Conectar la base de datos compartida.** Aquí el sistema deja de ser dos islas.
4. **Separar las dos vistas**: la del médico (catálogo y pedidos propios) y la de
   operación (todo lo demás).

Los pasos 1 y 2 no cambian nada de lo que ya funciona. El paso 3 es el que convierte
esto en una aplicación real y es el único que introduce una dependencia externa.
