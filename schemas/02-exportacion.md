# Schema 02 — Exportación desde SAP

Sacar datos de SAP en un layout definido para otro sistema o para revisión.

## El proceso

1. **Define qué vas a exportar** (documentos, saldos, maestros) y con qué filtros: sociedad, ejercicio, fechas, cuentas.
2. **Ejecuta la extracción** en SAP (reporte o transacción) con los campos del layout [schema-02-exportacion.csv](../layouts/schema-02-exportacion.csv).
3. **Exporta el resultado a archivo** (por ejemplo, desde el ALV a archivo local) y revisa que las columnas queden en el orden del layout.
4. **Valida el archivo**: encabezados completos, fechas e importes en el formato que pide el sistema destino, sin filas vacías.
5. **Entrégalo** al sistema destino o al área que lo pidió.

## Errores típicos

- Columnas en orden distinto al layout.
- Fechas o decimales en formato incorrecto.
- Caracteres especiales sin escapar.
- Filas duplicadas o vacías.
- Moneda o sociedad incorrecta.

## Nota

El layout es de ejemplo: los campos y formatos dependen del sistema que recibe los datos. Adáptalo antes de exportar.
