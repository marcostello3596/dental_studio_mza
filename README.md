# Dental Studio

Sitio web oficial de **Dental Studio** — odontología integral con mirada estética contemporánea, Mendoza · Argentina.

## Equipo

- **Marcos Tello** — Estética & rehabilitación (carillas, coronas, diseño de sonrisa)
- **Dolores Slysz** — Ortodoncia (tradicional y alineadores invisibles)

## Stack

Sitio estático, HTML/CSS/JS vanilla. Sin build step ni dependencias de npm. La home es una sola página; el blog son HTML sueltos.

Librerías cargadas desde CDN:

- **GSAP 3.12.5** + **ScrollTrigger** — animaciones y reveal on scroll
- **Lenis 1.0.42** — smooth scrolling
- **Google Fonts** — Lora (serif) + Poppins (sans)

## Estructura

```
.
├── index.html              # Home (HTML + CSS + JS inline)
├── site.css                # Estilos del blog
├── robots.txt
├── sitemap.xml
├── llms.txt                # Resumen para agentes de IA
├── blog/
│   ├── index.html
│   └── cada-cuanto-limpieza-dental/
│       └── index.html      # Nota de ejemplo / plantilla
├── ISOLOGO.png             # Isotipo de marca
├── EQUIPO.jpg              # Foto del equipo
├── CarillasAntes.JPG       # Caso clínico — antes
├── CarillasDespues.JPG     # Caso clínico — después
└── README.md
```

## Branding

Paleta nude & earth siguiendo el manual de marca v.01 (2026):

| Token   | Hex       | Rol                        |
| ------- | --------- | -------------------------- |
| Crema   | `#F4EBDF` | Fondo principal            |
| Marfil  | `#FAF6F0` | Fondo claro                |
| Ónix    | `#0E0E0E` | Tipografía / CTAs          |
| Arena   | `#E4D2BB` | Acento suave               |
| Tostado | `#B08968` | Contraste                  |
| Tierra  | `#6B4E3A` | Fondos profundos / footer  |

## Cómo correr

Abrir `index.html` en cualquier navegador moderno. La home no requiere servidor.

El blog usa rutas desde la raíz (`/blog/`, `/site.css`). Para verlo:

```sh
python3 -m http.server 8000
```

Después: `http://localhost:8000/`, `http://localhost:8000/blog/` y `http://localhost:8000/blog/cada-cuanto-limpieza-dental/`.

## Blog

Cada nota es HTML estático. No hay build. La carpeta `blog/<slug>/index.html` se publica en Vercel como `https://www.dentalstudiomza.com/blog/<slug>/`.

### Cómo agregar una nota

1. Copiá la carpeta `blog/cada-cuanto-limpieza-dental/` y renombrala con un slug en minúsculas, sin tildes ni espacios. Ejemplo: `blog/dolor-de-muela-que-hacer/`.
2. En el `index.html` nuevo, cambiá:
   - `<title>` y la meta description. Tienen que ser únicos y en español de Argentina.
   - `link rel="canonical"` y `og:url`, con la URL absoluta `https://www.dentalstudiomza.com/blog/<slug>/`.
   - Open Graph y Twitter: `og:title`, `og:description`, `twitter:title`, `twitter:description`.
   - El JSON-LD: `headline`, `description`, `datePublished`, `dateModified`, `mainEntityOfPage` y las tres URLs de `BreadcrumbList`. El `headline` tiene que ser idéntico al `<h1>`.
   - La miga de pan visible, la fecha (`<time datetime="AAAA-MM-DD">`) y el texto de la nota.
3. En `blog/index.html`, sumá una tarjeta (fecha, título, bajada y enlace) y el ítem en el JSON-LD, dentro de `blogPost`.
4. En `sitemap.xml`, agregá un `<url>` con `<loc>` igual al canonical.
5. En `llms.txt`, agregá el enlace en la sección Páginas, con una frase que diga de qué trata.
6. Revisá la nota con el servidor de arriba. Abrir el archivo suelto no resuelve las rutas que empiezan con `/`.

No inventes horarios, precios, dirección, nombres ni reseñas. Si un dato no está ya en el sitio, no lo pongas en la nota ni en el schema. El texto de salud es información general y la nota tiene que decirlo.

## Contacto

- WhatsApp: [261 253-3869](https://wa.me/5492612533869) (+54 9 261 253-3869)
- Teléfono: [0261 640-4194](tel:+542616404194)
- Email: [dentalstudiomza@gmail.com](mailto:dentalstudiomza@gmail.com)
- Instagram: [@dental.studio.mza](https://instagram.com/dental.studio.mza)
- Dirección: Julio A. Roca 403, 5ta Sección, Mendoza, Argentina

Los horarios de atención no están en el repositorio. No los agregues al sitio ni al schema hasta confirmarlos.
