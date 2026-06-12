# Dental Studio

Sitio web oficial de **Dental Studio** — odontología integral con mirada estética contemporánea, Mendoza · Argentina.

## Equipo

- **Marcos Tello** — Estética & rehabilitación (carillas, coronas, diseño de sonrisa)
- **Dolores Slysz** — Ortodoncia (tradicional y alineadores invisibles)

## Stack

Sitio estático single-page, HTML/CSS/JS vanilla. Sin build step ni dependencias de npm.

Librerías cargadas desde CDN:

- **GSAP 3.12.5** + **ScrollTrigger** — animaciones y reveal on scroll
- **Lenis 1.0.42** — smooth scrolling
- **Google Fonts** — Lora (serif) + Poppins (sans)

## Estructura

```
.
├── index.html              # Sitio completo (HTML + CSS + JS inline)
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

Abrir `index.html` en cualquier navegador moderno. No requiere servidor — funciona desde el filesystem.

Para desarrollo con live-reload (opcional):

```sh
npx serve .
# o
python3 -m http.server 8000
```

## Contacto

- WhatsApp: [+54 9 261 253-3869](https://wa.me/5492612533869)
- Instagram: [@dental.studio.mza](https://instagram.com/dental.studio.mza)
- Dirección: Julio A. Roca 403, 5ta Sección, Mendoza, Argentina
