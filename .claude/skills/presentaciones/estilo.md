# Estilo de las presentaciones

Cinematográfico, cálido y sobrio: poco texto y mucho movimiento. Los valores son
provisionales hasta contrastarlos con el CSS real de la web del autor.

## Color

| Token | Valor | Uso |
|---|---|---|
| ink | #121110 | Fondo de las diapositivas oscuras |
| ink-2 | #1E1B18 | Superficie elevada sobre ink |
| paper | #F5F2EC | Fondo de las diapositivas claras; texto sobre ink |
| on-light | #161513 | Texto sobre paper |
| amber | #E2A85B | Acento sobre ink; bloques destacados (texto encima en #161513) |
| amber-deep | #8F5414 | Acento sobre paper |
| soft-dark | #B8B0A4 | Texto secundario sobre ink |
| soft-light | #5B554D | Texto secundario sobre paper |

- Diseño cinematográfico: oscuro y claro alternos, empezando en oscuro.
- Un solo acento, en etiquetas, cifras y líneas; nunca en párrafos.

## Tipografía (Google Fonts)

- **Michroma**: titulares y cifras, en MAYÚSCULAS, con 4px de espaciado. Es muy ancha:
  unas 15 letras por línea a 112px y 18 a 88px.
- **Oswald 500**: etiquetas superiores, pies y botones, en mayúsculas, con 4–6px de espaciado.
- **DM Sans**: texto. Usa 500 en las frases destacadas.
- Escala: 220 (cifra) / 112 (portada) / 88 (título) / 44 (frase) / 32 (texto) /
  28 (etiqueta) / 24 (pie).

## Composición

- Lienzo de 1920×1080 con márgenes de 128px. La etiqueta va arriba a la izquierda
  y el titular debajo. El bloque visual se ancla abajo con `margin-top: auto`.
- Pie a 64px del borde inferior: el expositor a la izquierda y el número a la derecha.
- Portada y cierre centrados, con partículas, un recuadro de contorno de 2px y el
  nombre del expositor.
- Esquinas rectas en todo.

## Movimiento

- Partículas conectadas en portada, cierre y diapositivas de cifra.
- Entradas escalonadas: suben 40px en 0,8 s, con 140 ms de desfase entre elementos.
- Titulares de portada que pasan de desenfocados a nítidos.
- Cifras que cuentan desde 0.
- Puntos que recorren las líneas de los diagramas.
- La diapositiva completa ya se ve antes de 1 segundo.

## Voz

Frases cortas y afirmativas. Español, de tú con el público. Sin emojis ni
hashtags. Sin venta.
