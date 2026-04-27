# Reglas de diseño — Landing Somaflow

## Marca

- **Cliente:** Silvia Diazgranados
- **Producto:** Somaflow — programa de 30 días para regular el sistema nervioso desde el cuerpo
- **Enfoque:** psicología somática y neurociencia del trauma
- **Tono:** sereno, íntimo, orgánico. Sin tecnicismos ni urgencia de venta agresiva

---

## Paleta de colores

| Variable | Hex | Uso |
|---|---|---|
| `--noche` | `#2A3A34` | Fondo principal, secciones oscuras, nav |
| `--teal` | `#5FA484` | Acento principal, botones CTA, highlights |
| `--salvia` | `#D9E5CD` | Secciones claras alternadas |
| `--bosque` | `#416464` | Textos sobre salvia, iconos, bordes |
| `--crema` | `#F5F2EA` | Textos sobre fondos oscuros |
| `--musgo` | `#7A8C85` | Textos secundarios, subtítulos, nav izquierda |
| `--arena` | `#EDE9DF` | Fondos alternativos claros |
| `--bruma` | `#C8DDD6` | Bordes sutiles, detalles |
| `--eucalipto` | `#8DA992` | Detalles medios |
| `--olive` | `#B9C18F` | Acentos verdes cálidos |

### Regla de uso
- Fondos oscuros (`--noche`): texto en `--crema` o `--musgo`
- Fondos claros (`--salvia`, `--arena`): texto en `--bosque` o `--noche`
- Botones CTA siempre en `--teal` con texto blanco
- No usar negro puro ni blanco puro

---

## Tipografía

| Fuente | Uso | Peso |
|---|---|---|
| **Cormorant Garamond** (serif, italic) | Títulos h1/h2/h3, nombre de marca en nav, números de fase | 300 |
| **Jost** (sans-serif) | Cuerpo, labels, botones, texto de UI | 300 (cuerpo) / 500 (botones y labels) |

### Escala tipográfica
- H1 hero: 86px desktop / 48px mobile
- H2 sección: ~48–56px
- Tagline hero: 24px italic Cormorant
- Cuerpo: 18px Jost 300, line-height 1.65
- Labels uppercase: 12px Jost 500, letter-spacing 0.15em, con línea decorativa antes (`::before`)
- Números de fase: 80px Cormorant italic, blanco `rgba(255,255,255,0.15)`

---

## Iconos

- Estilo **hand-drawn / orgánico**: trazos a mano, bezier irregulares
- Atributos SVG obligatorios: `stroke-linecap="round"` `stroke-linejoin="round"` `fill="none"`
- Stroke-width: 1.5–2px
- Color: heredado (`currentColor`) para adaptarse al fondo
- No usar iconos geométricos perfectos ni librerías como Feather o Heroicons

---

## Layout y espaciado

- `max-width: 1200px` con `margin: 0 auto` y `padding: 0 24px` para el contenedor principal
- Padding de sección: `80px 24px` (desktop), `60px 24px` (mobile)
- Grids: 2 columnas en desktop, 1 columna en mobile (breakpoint 768px)
- Bordes redondeados en cards: `border-radius: 16px` o `24px`
- Gap entre cards: `16px`–`32px`

---

## Efectos y texturas

- **Grain overlay**: en hero, que-es, precio, cta y footer — SVG noise a `opacity: 0.035`
- **Wave dividers**: SVG de 80px entre secciones para transiciones suaves
- **Backdrop blur**: en nav (`blur(12px)`) y cards vidrio (`blur(4px)`)
- **Reveal on scroll**: clase `.reveal` con `opacity: 0` + `translateY(24px)`, visible con `.visible`
- **Aurora hero**: UnicornStudio, siempre visible a `opacity: 0.2`, se intensifica a `1.0` cuando el cursor está a menos de 220px del CTA
- **Hero video**: loop sin sonido, `object-fit: cover`, overlay `rgba(42,58,52,0.62)`

---

## Botones

| Tipo | Estilo |
|---|---|
| CTA principal | `background: var(--teal)`, `border-radius: 999px`, `padding: 18px 48px`, sombra teal |
| Pill nav | Mismo color, más pequeño: `padding: 10px 24px`, `font-size: 14px` |
| Hover | `translateY(-2px)` + sombra más intensa |

---

## Voz y tono del copy

- Primera persona del singular para Silvia, segunda para el usuario
- Frases cortas, sin jerga clínica excesiva
- Palabras clave del mundo: sistema nervioso, regulación, soma, cuerpo, tierra, base, ritmo
- Nada de urgencia artificial ("solo por hoy", "últimos cupos")
- Los CTAs invitan, no presionan: "Quiero empezar", "Empezar →"

---

## Lo que no hacer

- No usar sombras negras duras — siempre teal o transparentes
- No mezclar sans-serif distintos: solo Jost
- No usar iconos de línea perfecta o geométrica
- No poner texto blanco sobre `--salvia` (poco contraste)
- No comprimir el logo — siempre `width: auto` junto a la altura definida
