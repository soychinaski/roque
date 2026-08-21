# Diagnóstico por embudo

Léelo cuando el usuario traiga datos de una campaña que no funciona. El objetivo es localizar **dónde** se rompe antes de tocar nada, porque cada tramo se arregla de una forma distinta y tocar el tramo equivocado quema presupuesto sin aprender.

## Antes de diagnosticar

1. Confirma la **ventana de fechas** del Ads Manager. Un filtro mal puesto invierte diagnósticos completos.
2. Confirma que el elemento ha salido de fase de aprendizaje y lleva **al menos 7 días** o gasto equivalente a varios breakeven CPA.
3. Confirma que las exclusiones de placements están aplicadas. Si no lo están, ese es el diagnóstico y no hace falta seguir.

## Tabla síntoma → causa → acción

| Síntoma | Causa más probable | Acción |
|---|---|---|
| CTR por debajo del 1 % | El creativo no engancha, o el ángulo no le habla a nadie | Creativo nuevo con ángulo distinto, no variante cosmética |
| CTR muy alto (dos dígitos) y cero ATCs | Placements basura generando clics fraudulentos | Verificar exclusiones de Audience Network, Messenger, Threads |
| CTR normal, tráfico entrando, sin ATCs | Landing, precio, o desajuste entre lo que promete el ad y lo que se encuentra | Revisar coherencia ad→landing antes que tocar precio |
| ATCs sanos, sin compras | Checkout, confianza, gastos de envío sorpresa, métodos de pago | Hacer una compra de prueba completa uno mismo |
| Compras al principio y luego caída | Fatiga de creativo, o clon canibalizando al original | Frecuencia y CPM del original en ventana de 7 días |
| CPM disparado sin cambiar nada | Subasta más cara (temporada, competencia) o señal de calidad de cuenta | No reaccionar en caliente: ventana de 7 días |
| Todo cae a la vez en todas las campañas | Casi nunca es la campaña | Revisar tracking, píxel, pasarela de pago y estado de la cuenta antes de tocar nada |

## Fatiga: cómo se confirma

La fatiga **no** es un mal día. Se confirma cuando, en ventana de 7 días y de forma sostenida:

- la frecuencia sube por encima de 2,5–3,
- **y** el CPA se deteriora,
- **y** el CTR baja respecto a sus propias primeras semanas.

Los tres a la vez. Uno solo no es fatiga.

La respuesta a la fatiga es **creativo nuevo**, no bajar el presupuesto. Bajar el presupuesto de un creativo quemado solo alarga la agonía.

## Errores de lectura que cuestan dinero

- **Leer días sueltos.** El día es la unidad de la ansiedad, no del análisis.
- **Leer un creativo con 2 días.** Fase de aprendizaje más atribución sin madurar.
- **Atribuir a la última variable tocada** cuando se tocaron dos.
- **Comparar ventanas de distinta longitud** (últimos 3 días contra últimos 14) y concluir tendencia.
- **Concluir sin mirar el mix de productos.** Un CPA subiendo puede ser un mix moviéndose hacia la variante barata, con el negocio igual de sano.
