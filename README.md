# ROQUE

**Tu media buyer senior de Meta Ads dentro de Claude Code.**

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

### Windows (PowerShell)

Copia y pega estas cuatro líneas, una a una:

    cd $env:TEMP
    Invoke-WebRequest "https://github.com/soychinaski/roque/archive/refs/heads/main.zip" -OutFile roque.zip
    Expand-Archive roque.zip -DestinationPath . -Force
    Copy-Item ".\roque-main\roque" -Destination "$env:USERPROFILE\.claude\skills\" -Recurse -Force

Si te dice que no existe la carpeta de destino, créala antes:

    mkdir "$env:USERPROFILE\.claude\skills" -Force

Y comprueba que quedó bien:

    Get-ChildItem "$env:USERPROFILE\.claude\skills\roque" -Recurse | Select-Object FullName

### macOS y Linux (Terminal)

    cd /tmp
    curl -L https://github.com/soychinaski/roque/archive/refs/heads/main.zip -o roque.zip
    unzip -o roque.zip
    mkdir -p ~/.claude/skills
    cp -r roque-main/roque ~/.claude/skills/

Y comprueba:

    ls -R ~/.claude/skills/roque

En ambos casos te tienen que quedar cuatro cosas: `SKILL.md`, la carpeta `references/` y dentro `diagnostico.md` y `cuenta-e-identidad.md`.

## Primer uso

Abre Claude Code y suéltale una pregunta real, sin nombrar la skill:

> tengo un ad set con 280 € gastados y 9 compras, ¿escalo o espero?

ROQUE se activa solo, calcula el CPA y te dice que no puede decidir nada sin tu breakeven ni la ventana de fechas. Eso no es un fallo: es el producto funcionando.

**No rellenes `contexto.md` a mano.** Dile:

> móntame el contexto.md, te voy dando los datos

Y te lo construye preguntándote lo que hace falta — empezando por el breakeven CPA, que es el número del que cuelga todo lo demás. Guárdalo en la carpeta del proyecto desde el que trabajes y mantenlo vivo: cuando cambie un precio, un coste o un geo, cámbialo ahí.

## Lo que no es

- No genera creativos ni copy.
- No busca productos.
- No monta tiendas, píxeles ni CAPI.
- No conecta con la API de Meta: tú le pasas los datos, él razona sobre ellos.

Hace una cosa: **comprar tráfico en Meta con criterio**.

## Aviso

Los umbrales que trae son puntos de partida sacados de operación real, no verdades universales. Tu breakeven manda siempre. Y las reglas de plataforma cambian: lo que aquí se da por válido tiene fecha.
