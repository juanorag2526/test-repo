---
name: presentaciones
description: Crea presentaciones 16:9 completas con el estilo de Juan Ramiro Alvarado Gómez a partir de un tema, unas notas o archivos (PDF, Word, PowerPoint, Excel, texto, imágenes): extrae las ideas clave, arma la historia según el tipo y la duración, diseña las diapositivas con su sistema (Michroma, Oswald, DM Sans, ámbar, partículas, cifras que cuentan) y entrega dos cosas, la presentación editable en Diapositivas y la versión en vivo con controles para el escenario (pasador, cronómetro, notas, pantalla en negro). Úsala cuando alguien diga «hazme una presentación», «convierte este documento en diapositivas», «prepara mi charla», «necesito unas slides para…», «pásame esto a presentación», «haz el deck de…». No es para la imagen de un post de LinkedIn (usa linkedin-infografia).
---

# Presentaciones

Cada presentación sale del mismo proceso y con el mismo estilo. No hay límite de
presentaciones: cada una es un artefacto nuevo.

Estilo: `estilo.md` (léelo siempre). Sistema de diseño publicado:
https://claude.ai/artifact/Nh4h7Hj39rPPpr5pA5jin8. Ejemplo terminado:
`ejemplo/` («Los 3 niveles de la IA», 8 diapositivas, 10 minutos).

## 1 · El encargo (una sola ronda de preguntas)

Si falta algo, pregúntalo todo junto, una vez. Si la persona ya lo dijo o no
contesta, usa los valores por defecto y dilo en una línea.

| Dato | Por defecto |
|---|---|
| Tipo: charla, clase, propuesta, informe, pitch, formación interna o libre | charla |
| Duración | 10 minutos |
| Público | el que se deduzca del material |
| Mensaje final | lo propones tú desde el material |
| Lo que no quiere | sin fotos, sin precios, sin datos inventados, poco texto |
| Diseño: cinematográfico (oscuro y claro alternos), oscuro o claro | cinematográfico |
| Expositor | Juan Ramiro Alvarado Gómez |

Número de diapositivas según la duración: 5 min → 6 · 10 → 8 · 15 → 10 · 20 → 12 ·
30 → 15.

## 2 · El material

- **Archivos:** léelos enteros (PDF, Word, PowerPoint con sus notas, Excel, CSV,
  texto, imágenes). Si uno no se puede leer (formatos .doc/.ppt antiguos, PDF
  escaneado, audio o vídeo), di cuál y pide PDF, texto o una imagen.
- **Sin archivos:** trabaja con lo que diga la persona. No busques cifras por tu
  cuenta salvo que lo pida, y entonces cita la fuente.
- **Si prefiere subirlos ella sola:** el Creador de presentaciones hace lo mismo
  en una página: https://claude.ai/artifact/CBWU3Uvp5JZhGn1xVFajad

Escribe primero las **ideas extraídas** (de 3 a 6 frases) y enséñalas.

## 3 · La historia

Estructura según el tipo:

| Tipo | Recorrido |
|---|---|
| Charla | lo que frena → es normal → la idea central → su desarrollo en pasos o niveles → cierre memorable |
| Clase | objetivo → conceptos uno a uno → ejemplo → cómo aplicarlo → resumen → reto |
| Propuesta | situación → problema y su costo → solución → cómo funciona → resultados esperados → próximos pasos |
| Informe | resumen en una frase → cifras clave → qué funcionó → qué no → aprendizajes → próximos pasos |
| Pitch | problema → solución → para quién → cómo funciona → evidencia → modelo → equipo → lo que pides |
| Formación interna | por qué importa → proceso paso a paso → errores comunes → buenas prácticas → resumen |

Entrega el guion en una tabla (n.º, layout, título, idea, tiempo) y sigue sin
esperar, salvo que la persona haya pedido revisarlo.

Reglas del guion:
- Una idea por diapositiva. Primera: `cover`. Última: `closing`.
- Un layout visual (cards, steps, flow, number) al menos cada dos diapositivas y
  nunca el mismo layout dos veces seguidas.
- Cifras solo del material, con su fuente en la diapositiva. Si no hay ninguna,
  vale una que sea cierta por definición (el 100 % de los expertos fue
  principiante); nunca una inventada.
- Notas del orador en cada diapositiva: 2 o 3 frases en primera persona, con la
  franja de tiempo (por ejemplo, «4:30–6:00»).

## 4 · La presentación editable (Diapositivas)

1. `Artifact` → `quickstart` con `intent: "slides"` y crea la presentación desde
   el tipo Diapositivas, sin sistema de diseño (no hay ninguno en la cuenta).
2. Copia `ejemplo/deck.css` tal cual a `project/deck.css` y usa sus clases. Las
   fuentes de `ejemplo/deck.json` (`faces`) van igual.
3. Cada slide se escribe como los de `ejemplo/slides/`:
   - `portada.html` y `copiloto.html`: portada y cierre con partículas (`<x-embed>`).
   - `frena.html`: tarjetas (cards).
   - `normal.html`: cifra que cuenta (`<p class="n">`).
   - `niveles.html`: escalera (steps).
   - `nivel1.html`: conversación.
   - `nivel2.html`: una idea que se reparte en varias (abanico con puntos en movimiento).
   - `nivel3.html`: proceso (flow).
4. Pie con el nombre del expositor y el número en todas menos portada y cierre.
   En portada y cierre, el nombre va bajo la etiqueta.
5. Vista previa una vez (ver las instrucciones del tipo) y corrige lo que se corte.

## 5 · Versión en vivo (para el escenario)

1. Copia `en-vivo.html` a `presentaciones/<AAAA-MM-DD>-<tema>/en-vivo.html`.
2. Cambia solo `<title>` y el objeto `DATOS` (no toques el motor):

```json
{"title":"…","speaker":"Juan Ramiro Alvarado Gómez","duration":10,"style":"alterna|oscuro|claro",
 "slides":[
  {"layout":"cover","eyebrow":"…","title":"…","subtitle":"…","tag":"…","notes":"…"},
  {"layout":"statement","eyebrow":"…","title":"…","text":"…","notes":"…"},
  {"layout":"cards","eyebrow":"…","title":"…","items":[{"title":"…","text":"…"}],"notes":"…"},
  {"layout":"steps","eyebrow":"…","title":"…","items":[{"title":"…","text":"…"}],"notes":"…"},
  {"layout":"flow","eyebrow":"…","title":"…","text":"…","items":[{"title":"…"}],"notes":"…"},
  {"layout":"number","eyebrow":"…","value":"159101","suffix":"","label":"…","source":"archivo","notes":"…"},
  {"layout":"quote","eyebrow":"…","text":"…","source":"…","notes":"…"},
  {"layout":"closing","eyebrow":"…","title":"…","subtitle":"…","tag":"…","notes":"…"}]}
```

   Límites de caracteres: title ≤ 26 (≤ 34 en cover y closing), eyebrow ≤ 32,
   text ≤ 120, items[].title ≤ 28, items[].text ≤ 80. cards: 2–4 ítems; steps:
   3–4; flow: 3–5. En `value`, solo el número.
3. Publícala como artefacto (página HTML, icono `slides`).

La versión en vivo tiene una barra discreta que se oculta sola. Controles:
- Flechas, Av Pág/Re Pág o espacio para avanzar y retroceder (también con pasador).
- Clic en la pantalla: tres cuartos derechos avanza, el cuarto izquierdo retrocede.
- 1–9 salta a esa diapositiva.
- B: pantalla en negro. N: notas. P: pausa el cronómetro. T: lo reinicia. F: pantalla completa.

## 6 · Entrega

- Enlace de la editable y enlace de la versión en vivo.
- Las ideas extraídas y lo que supusiste (en una línea cada cosa).
- Los marcadores que falten, si los hay (`[cifra]`, `[nombre]`).
- Recuerda que los artefactos son privados hasta que se comparten.
- Guarda el guion en `presentaciones/<AAAA-MM-DD>-<tema>/guion.md`.

## Nunca

- Fotos, precios u ofertas si la persona no los pide.
- Cifras, citas, clientes o fuentes inventadas.
- Política partidaria o nombres de personas (reglas del perfil en `linkedin/perfil.md`).
- Más de una idea por diapositiva o párrafos largos.
