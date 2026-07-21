# Felpudos y Servicios — Notas de contexto

Fuente: Flyer de precios 2026, carta de presentación, y 3 cotizaciones reales (Vet. Orbegoso, FINA, Bar Popular). Archivos originales en `documentos/`.

## Datos legales y de contacto
- **Nombre comercial:** Felpudos y Servicios
- **Razón social:** Felpudos y Películas S.A.C.
- **RUC:** 20512620265
- **+20 años de experiencia** en el mercado peruano
- **Dirección:** Av. Alfredo Benavides 3663, Oficina 603, Santiago de Surco, Lima
- **Teléfono/Cel:** 996017068 (proformas) · WhatsApp cotizaciones: 998 613 326 (flyer)
- **Email:** felpudosyservicios@gmail.com (proformas/uso comercial) · felpudosypeliculas@gmail.com (aparece en el flyer, a verificar cuál es el vigente)
- **Representante:** Raúl Vásquez Sigarróstegui — Gerente General (firma como "Raúl Vásquez S.")
- **Banco:** Scotiabank Ahorros S/ 044-8054-114 · CCI 009-230-2004480-54114-43, a nombre de Felpudos y Películas SAC

## Logo oficial (IMPORTANTE — distinto al del sitio web actual)
El logo real usado en cotizaciones y flyers es un ícono de felpudo en perspectiva con rayas diagonales, más el badge cuadrado con una "F", y el texto "FELPUDOS" / "Y SERVICIOS" en dos colores. **Esta paleta NO coincide con la del `index.html` actual del repo** (que usa navy/rojo/dorado genérico). Colores reales extraídos del logo (`logo_oficial_extraido.png`):

| Elemento | Color aprox. | Hex |
|---|---|---|
| Rayas/base del felpudo (dorado) | Amarillo dorado | `#FAB035` |
| Franja inferior del felpudo | Naranja | `#F58038` |
| Contorno, badge "F", texto "Y SERVICIOS" | Teal/petróleo | `#005E7D` (rango `#005E7D`–`#006277`) |
| Texto "FELPUDOS" | Magenta/rosa | `#C2266B` |
| Fondo | Blanco | `#FFFFFF` |

**Recomendación:** si se quiere consistencia de marca, el sitio web (`index.html`) debería migrar a esta paleta real (teal + dorado/naranja + magenta) en vez de la navy/rojo/dorado que tiene ahora, ya que es la que ven los clientes en cotizaciones formales.

## Portafolio de productos (ampliado vs. lo que ya estaba en el sitio)
1. **Felpudo de Vinilo Atrapamugre** (Alto Tránsito) — 14mm, marca base "Confort Mat" — desde S/110 (1.20×0.90m)
2. **Felpudos Mixtos** (limpian y secan, perfil de jebe) — 15mm, gris oscuro jaspeado — S/200 (1.20×1.06m) / S/250 (1.60×1.06m) / S/280 (1.80×1.06m)
3. **Piso Antifatiga** — 9mm S/120 / 13mm S/200 (1.50×0.90m), superficie antideslizante
4. **Felpudos personalizados con logo** — hechos a mano, medidas típicas 1.20×0.90m / 1.60×1.20m / 1.80×1.20m
5. **Alfombras para oficinas corporativas** (mencionado en carta de presentación — no estaba en el catálogo web)

## Precios reales de felpudos personalizados (ejemplos de cotizaciones 2026)
| Cliente | Medida | Detalle | Precio |
|---|---|---|---|
| Veterinaria Orbegoso | 1.20×0.90m, 15mm, logo 0.60×0.70 | Base gris, logo rojo/negro | S/320 |
| FINA (Zyra Grupo Inmobiliario) | 1.20×0.90m, 15mm, logo 0.60×0.70 | Base negra, diseño circular + letras oro 13cm | S/410 |
| Bar Popular | 1.20×1.00m, 14mm, logo 1.00m ancho | Base gris, logo negro/rojo + S/20 delivery Surquillo | S/360 + S/20 |

El precio del personalizado varía según tamaño de base, grosor y complejidad/tamaño del logo (rango observado: S/320–410 solo por la pieza).

## Condiciones comerciales estándar (todas las cotizaciones)
- **Forma de pago:** Adelanto 50% + saldo contra entrega
- **Entrega:** 2–3 días hábiles desde el pago del adelanto
- **Garantía:** 1 año por falla de fabricación
- **Vigencia de precio:** 15 días
- Precios incluyen IGV

## Clientes / cartera de referencia
TGI Fridays (foto de portada del flyer), Veterinaria Orbegoso, FINA / Zyra Grupo Inmobiliario, Bar Popular — más "amplia cartera de clientes a nivel nacional" (carta de presentación).

## Uso futuro
El usuario mencionó que compartirá más cotizaciones para que más adelante se le ayude a automatizar/gestionar ese proceso (generación de proformas, seguimiento, etc.).

## Cotizador de costeo (Excel)

`herramientas/Felpudos_Cotizador.xlsx` (v2) — transcripción a Excel de las notas de costeo
manuscritas del usuario (fotos compartidas el 2026-07-21, no guardadas como archivo porque se
pegaron directo en el chat en vez de adjuntarse). Contiene 3 pestañas:

- **Datos Base:** tabla única de materiales (Confort Mat, Multilop, Paolo, Q Rubber) en S//m²,
  tabla de niveles de complejidad de logo (Simple/Media/Compleja), y las tarifas de Mixtos y
  Piso Antifatiga.
- **Cotizador:** calculadora con inputs — ancho, alto, **marca y espesor (siempre activo, con o
  sin logo)**, ¿lleva logo?, **complejidad del logo (Simple/Media/Compleja)** si aplica, y margen
  deseado — que calcula el precio sugerido automáticamente. Cubre las 3 líneas: Felpudo de Vinilo
  (con o sin logo), Felpudos Mixtos, Piso Antifatiga.
- **Notas y Supuestos:** documenta cómo se derivaron las fórmulas y los puntos a validar.

**Cambio de diseño (v2, pedido por el usuario):** antes la marca/espesor solo se usaba cuando el
felpudo NO llevaba logo (con logo se asumía siempre "Confort Mat"). Ahora la marca/espesor se
elige siempre, independiente del logo, y la complejidad del logo es un factor aparte con su
propio impacto en costo de material y mano de obra.

**Pendiente clave — sin datos reales:** solo el nivel de complejidad "Media" está calibrado con
los 4 ejemplos manuscritos reales. Los multiplicadores de "Simple" (×0.6 material / ×0.7 mano de
obra) y "Compleja" (×1.5 material / ×1.4 mano de obra) son **estimaciones** marcadas en ámbar en
la pestaña Datos Base — ajustar en cuanto el usuario comparta cotizaciones reales de logos
simples y complejos.

Otros supuestos pendientes de validar (ver pestaña Notas y Supuestos del Excel):
- Conversión de S//m lineal a S//m² para Multilop/Paolo/Q Rubber (÷1.20m de ancho de rollo) —
  asume que un corte más angosto cuesta proporcionalmente lo mismo por m².
- La regla de "longitud extra de ribete" (0.20m vs 0.30m) se infirió de los 4 ejemplos, no está confirmada.
- El costo de Paolo 15mm aparece como S/90 en una sección de la foto y S/95 en otra (se usó S/95).
- La mano de obra de Felpudos Mixtos se interpoló con solo 3 puntos — es la fórmula menos confiable.

**Pendiente:** validar estos supuestos con el usuario y, si se comparten más ejemplos reales de
cotizaciones, recalibrar las fórmulas en la pestaña "Datos Base" (el Cotizador se actualiza solo).
