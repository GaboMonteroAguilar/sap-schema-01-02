# Schema 01 — Importación a SAP

Cargar datos a SAP con un archivo y LSMW (Legacy System Migration Workbench).

## El proceso

1. **Prepara el archivo** con el layout [schema-01-importacion.csv](../layouts/schema-01-importacion.csv): una fila por línea del documento, mismo documento agrupado por los campos de encabezado (sociedad, fecha, tipo de documento, referencia).
2. **Crea el objeto LSMW** (proyecto, subproyecto, objeto) para el tipo de dato a cargar.
3. **Define la estructura de origen** con los campos del archivo.
4. **Mapea los campos** de origen a los campos de SAP (sociedad, cuenta, importe, moneda, fechas, centro de costo, texto).
5. **Lee y convierte los datos** en LSMW y revisa el archivo convertido.
6. **Ejecuta la carga** (batch input, direct input o BAPI, según el objeto) y revisa el log.
7. **Corrige los errores** del log y vuelve a cargar solo los registros fallidos.

## Errores típicos

- Formato de fecha o decimales distinto al de SAP.
- Campos obligatorios vacíos (sociedad, cuenta, moneda, fecha).
- Documento descuadrado: débitos distintos a créditos.
- Cuenta o centro de costo inexistente.
- Periodo contable cerrado.
- Moneda o tipo de documento incorrecto.

## Nota

Los campos exactos dependen del objeto y la transacción que uses (por ejemplo, documento FI). Adapta el layout a tu configuración antes de cargar.
