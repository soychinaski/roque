# ROQUE

**Tu media buyer senior dentro de Claude.**

ROQUE no es una herramienta ni un generador de anuncios. Es el criterio de un comprador de tráfico con años de cuenta a sus espaldas, escrito en archivos que tu Claude lee antes de contestarte. Le pones tus números y a partir de ahí te dice qué mirar, en qué orden y cuándo decidir — incluida la respuesta que menos gusta, que es "no toques nada y espera a que cierre la ventana".

## Para quién es

Para quien ya está comprando tráfico en Meta y toma decisiones con dinero encima de la mesa. No explica qué es un ROAS ni cómo se abre un Business Manager: da por hecho que eso lo sabes. Si estás empezando desde cero, esto te va a quedar grande y no pasa nada.

## Qué hace distinto

La mayoría de los prompts de marketing te dan una opinión rápida. ROQUE hace lo contrario: **antes de opinar te pide la ventana de fechas, el gasto, el CTR, los ATCs y el AOV**, y si no los tienes, te dice que no hay diagnóstico posible. Ese es todo el truco. La diferencia entre perder dinero y no perderlo casi nunca está en saber más, está en no decidir con dos días de datos.

Dentro hay:

- **Doctrina de estructura** — qué se lanza, qué se excluye siempre y por qué el targeting real lo hace el creativo.
- **Rondas** — una variable por ronda, ventanas de 7 días, escalado por tramos, clones tratados como el test que son.
- **Kill criteria** — escritos antes de lanzar, calculados sobre tu breakeven, no sobre el de otro.
- **Diagnóstico por embudo** — tabla de síntoma → causa → acción, para dejar de tocar el tramo equivocado.
- **Salud de cuenta** — identidad, claims y política, que es donde se pierden las operaciones enteras.

## Instalación

1. Descarga o clona este repo.
2. Copia la carpeta `roque/` dentro de tu carpeta de skills de Claude Code:
   - macOS / Linux: `~/.claude/skills/`
   - Windows: `C:\Users\TU_USUARIO\.claude\skills\`
3. Copia `contexto.md` a la carpeta del proyecto desde el que trabajes.
4. **Rellena `contexto.md`.** Sobre todo el breakeven CPA. Sin ese número ROQUE no puede diagnosticar nada y te lo va a decir.
5. Abre Claude Code y pregúntale algo real: *"tengo un ad set en 340 € gastados, 12 compras, CTR 2,1 %. ¿Escalo?"*

## Lo que no es

- No genera creativos ni copy.
- No busca productos.
- No monta tiendas, píxeles ni CAPI.
- No conecta con la API de Meta: tú le pasas los datos, él razona sobre ellos.

Hace una cosa: **comprar tráfico en Meta con criterio**.

## Aviso

Los umbrales que trae son puntos de partida sacados de operación real, no verdades universales. Tu breakeven manda siempre. Y las reglas de plataforma cambian: lo que aquí se da por válido tiene fecha.
