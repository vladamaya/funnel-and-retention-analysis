# Análisis de embudo y retención para MercadoLibre con SQL

Proyecto de portafolio — TripleTen Data Analyst, Sprint 4: Analiza journeys de usuarios con SQL (Proyecto 4).

## En simple

Un "journey" es el camino que sigue una persona en una tienda en línea: entra, escoge un producto, lo agrega al carrito, empieza a pagar y compra (o se sale en el camino).

En este proyecto medí cuánta gente avanza en cada paso de ese camino, por país, para ver dónde se pierde más gente.

## Qué hice

- Construí el embudo de compra paso a paso: first_visit → select_item → add_to_cart → begin_checkout → add_shipping_info → add_payment_info → purchase
- Segmenté el embudo por país (country)
- Analicé retención por país y por cohorte (grupos de usuarios según cuándo entraron)
- Entregué un informe ejecutivo en Google Sheets

## Herramientas

- SQL (PostgreSQL)
- Google Sheets (informe ejecutivo)

## Consulta principal

Ver [`proyecto4_embudo_por_pais.sql`](./proyecto4_embudo_por_pais.sql) — consulta aprobada en TripleTen, Parte 2: Construir el embudo de conversión, Tarea 3: Segmentar el Embudo General por país.

## Resultados clave

Del informe ejecutivo en la hoja entregada (periodo 2025-01-01 a 2025-08-31):

- **Embudo general:** la mayor caída ocurre de `select_item` a `add_to_cart`: la conversión baja de 76.90% a 11.01% (65.89 puntos porcentuales; se pierde el 85.70% de quienes seleccionaron producto).
- **Por país:** la mayor pérdida en ese paso es en Perú (de 84.55% a 10.00%, caída de 74.55 pp), seguido de Bolivia (70.97 pp) y Colombia (66.66 pp). La menor caída es en Uruguay (59.09 pp), que además tiene la mejor conversión a compra (4.55%); se debe validar el tamaño de muestra de Uruguay antes de concluir que su desempeño es superior.
- **Retención por cohorte** (cohortes de enero a junio de 2025, promedio D7/D14/D21/D28): 86.6% / 55.4% / 25.0% / 2.6%. La mayor reducción ocurre entre D21 y D28 (22.3 pp).
- **Retención por país (líderes por periodo):** D7 Brasil (87.2%), D14 y D21 México (55.8%), D28 Perú (3.2%); el nivel más bajo en D28 es Colombia (1.6%).
- **Reflexión:** la etapa a mejorar primero es `select_item` → `add_to_cart` (solo ~11% agrega al carrito frente a ~76% que selecciona producto); los usuarios muestran interés inicial, pero pocos completan la compra y la retención disminuye con el tiempo.

## Entregable

Google Sheet: [Proyecto 4: Análisis de embudo y retención para MercadoLibre](https://docs.google.com/spreadsheets/d/1JIqOrvWeUS5f-gNyapKFziCgFf5Wb-gKeQT1YjJMwpo/edit?usp=edit)
Pestañas: Informe Ejecutivo, Embudo General, Embudo General x Pais, Retencion x Pais, Retencion x Cohort.

Nota de alcance: la consulta incluida en este repo es la del embudo segmentado por país; el análisis de retención por país y por cohorte está en las pestañas correspondientes de la hoja entregada.

## Notas

- Periodo de los eventos en la consulta: 2025-01-01 a 2025-08-31
- Tabla usada: `mercadolibre_funnel` (datos del entorno de práctica de TripleTen; los datos crudos no se incluyen en este repositorio)
- Proyecto aprobado en TripleTen (Iteración 1)

## Autor

Vlad — Analista de datos en formación (TripleTen).
