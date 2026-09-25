# Datos abiertos — Observatorio Frontera Sur

Cifras oficiales de llegadas irregulares a España, tal como las publican el
**Ministerio del Interior** (informes quincenales) y **Frontex** (detecciones mensuales),
normalizadas y regeneradas cada mañana desde [fronterasur.es](https://fronterasur.es).

| Fichero | Contenido |
|---|---|
| `llegadas_quincenales.csv` | Una fila por periodo publicado por Interior desde julio de 2024: fechas, días, llegadas, por zona (Canarias, Península, Baleares, Ceuta, Melilla), revisiones de la fuente y zonas sin actualizar |
| `acumulados_interior.csv` | Una fila por informe quincenal desde 2022: acumulado a esa fecha por vía y zona, y la cifra del año anterior a igual fecha |
| `frontex_mensual.csv` | Una fila por mes desde enero de 2009: detecciones en las dos rutas que llegan a España |
| `data.json` | Todo lo que usa la web: último informe, quincenas, anuales, zonas, Frontex (rutas, meses, nacionalidades, Europa) |

CSV con separador `;`, coma decimal y UTF-8 con BOM: se abren directamente en Excel en español.

## Lo que hay que saber antes de usarlos

- **No existe un dato diario.** Interior publica cada quince días un acumulado desde el 1 de enero. Las medias diarias son medias de periodos cerrados.
- **Las cifras de Interior son provisionales** y la fuente las revisa. Cuando el acumulado de una zona baja de un informe al siguiente, es una revisión, no que no llegara nadie: va en la columna `revision_*`.
- **Cuando Interior no actualiza una zona en un informe** (pasó con Ceuta el 15-09-2026: la página del informe seguía fechada al 31 de agosto con la misma cifra), la celda va vacía y la zona aparece en `zonas_sin_actualizar`. Un cero sería falso.
- **Interior y Frontex no se suman.** Interior cuenta personas llegadas; Frontex, detecciones de cruce (una persona puede contarse dos veces).

## Fuente, licencia y cita

Los datos son de sus organismos y se reutilizan conforme al
[Real Decreto 1495/2011](https://www.boe.es/buscar/act.php?id=BOE-A-2011-17560) y a las
condiciones de Frontex (reutilización autorizada citando la fuente). Este repositorio no
añade ninguna licencia propia ni puede darla. Cita siempre la fuente original:

> Ministerio del Interior, *Informe quincenal de inmigración irregular*. Frontex, *Monthly
> detections of illegal border-crossings*. Consultados en Observatorio Frontera Sur, fronterasur.es.

Sitio independiente: no está afiliado al Ministerio del Interior ni a Frontex, y ninguno de
los dos participa, patrocina ni respalda este repositorio. Metodología completa:
[fronterasur.es/metodologia](https://fronterasur.es/metodologia/). Contacto: contacto@fronterasur.es.
