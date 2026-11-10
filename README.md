# Schemas SAP 01 y 02 — Importación y Exportación

Layouts y guías para importar y exportar datos en SAP.

## Schemas

- **Schema 01 — Importación** ([guía](schemas/01-importacion.md) · [layout](layouts/schema-01-importacion.csv)): cargar datos a SAP con LSMW.
- **Schema 02 — Exportación** ([guía](schemas/02-exportacion.md) · [layout](layouts/schema-02-exportacion.csv)): sacar datos de SAP en un layout definido.

## Cómo usar

1. Llena el layout con tus datos, sin cambiar los encabezados.
2. Revisa que los campos obligatorios vengan completos y que los documentos cuadren (débitos = créditos en importación).
3. Sigue la guía del schema que corresponda.

## Nota

Los layouts son de ejemplo: los campos y formatos dependen de la configuración de tu SAP y del sistema que recibe o entrega los datos. Adáptalos antes de cargar.
