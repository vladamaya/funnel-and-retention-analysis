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
