# Catálogo web — Altok 3D

Página de una sola pantalla con los productos, precios de referencia y botón
directo a WhatsApp. Pensada para ir en el link de la bio de Instagram.

Es **estática** (solo HTML y CSS), así que se puede publicar gratis en GitHub
Pages y no necesita servidor ni base de datos.

---

## 1. Cambia el número de WhatsApp (lo primero)

Abre `index.html` y busca `56900000000`. Aparece **dos veces**: en el botón de
la sección de contacto y en el botón flotante verde.

Reemplázalo por tu número en este formato: código de país + celular, sin el
signo `+`, sin espacios ni guiones.

```
Ejemplo: para +56 9 1234 5678  ->  56912345678
```

## 2. Pon tus fotos

En la carpeta `img/` hay una imagen por producto, con el nombre que espera la
página. Reemplaza cada archivo por tu foto, **manteniendo el mismo nombre**:

| Archivo | Producto |
|---|---|
| `organizador-te.jpg` | Organizador de té |
| `soporte-control.jpg` | Soporte para control |
| `soporte-cartas.jpg` | Soportes para cartas |
| `deckbox.jpg` | Deckbox personalizado |
| `figuras.jpg` | Figuras y articulados |
| `llaveros.jpg` | Llaveros personalizados |
| `organizadores.jpg` | Organizadores |
| `empresas.jpg` | Para tu negocio |

Recomendaciones para las fotos:

- **Horizontales** y de tamaño parecido entre sí (la página las recorta a 4:3)
- Alrededor de **1200 px de ancho**: se ven nítidas y no pesan de más
- **Mismo fondo y misma luz en todas** — es lo que hace que el catálogo se vea
  profesional, más que la calidad de cada foto por separado

## 3. Ajusta productos y precios

Cada producto es un bloque `<article class="tarjeta">` dentro de `index.html`.
Para cambiar uno, edita el título, la descripción y el precio. Para agregar
otro, copia un bloque completo y cambia sus datos.

Los precios dicen "desde" a propósito: son referenciales y el valor final lo
defines al cotizar.

---

## Publicar gratis en GitHub Pages

1. Crea un repositorio **público** llamado `altok-catalogo` en GitHub
   (público es necesario para que Pages funcione en cuentas gratuitas)
2. Sube el proyecto:

```bash
git remote add origin https://github.com/TU_USUARIO/altok-catalogo.git
git push -u origin main
```

3. En GitHub: **Settings → Pages → Source: Deploy from a branch → main → /(root)**
4. A los pocos minutos queda disponible en:
   `https://TU_USUARIO.github.io/altok-catalogo/`

Esa dirección es la que va en el link de tu bio de Instagram.

> **Ojo:** este repositorio es público, así que no pongas acá nada privado.
> Los datos de clientes, costos y márgenes viven en el panel interno, que es
> otro repositorio y es privado.

## Ver la página en el computador

```bash
python -m http.server 8080
```

Y abre `http://localhost:8080` en el navegador.
