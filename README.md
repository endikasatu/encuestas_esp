# 📊 Encuestas en España

[![GitHub commit](https://img.shields.io/github/license/endikasatu/encuestas_esp)](https://github.com/endikasatu/catalunya-2021-model/blob/main/LICENSE) [![GitHub commit](https://img.shields.io/github/last-commit/endikasatu/encuestas_esp)](https://github.com/endikasatu/catalunya-2021-model/blob/main/LICENSE) 

Todas las encuestas públicas para las próximas elecciones generales, autonómicas y municipales en España recogidas por TheElectoralReport.

Consulta todas las encuestas en [TheElectoralReport](https://electoralreport.com/encuestas/).

Creado por [Endika Nuñez](twitter.com/endikasatu).

## Archivos disponibles

Este repositorio mantiene actualizados 3 archivos .csv.

- **data/spain_latest_polls.csv**: Todas las encuestas.
- **data/last2monthsPolls.csv**: Todas las encuestas de los últimos dos meses.
- **data/polls_update.csv**: Fecha de la última actualización.
- **src/polls_src.csv**: Fuente para el *scraping* de las encuestas desde la Wikipedia.

## Variables

- `Tipo`: Tipo de elección.
- `Literal`: El lugar donde se realiza la encuesta.
- `CCAA`: La comunidad autónoma donde se realiza la encuesta.
- `Provincia`: La provincia donde se realiza la encuesta.
- `Municipio`: El municipio donde se realiza la encuesta.
- `Encuestadora/Medio`: Encuestadora encargada de realizar el sondeo o el medio que lo difunde.
- `Fuente`: Enlace a la fuente donde se ha publicado la encuesta.
- `Muestra`: El número de entrevistas realizadas.
- `Trabajo Campo`: Fecha de realización del trabajo de campo.
- `Último día`: El último día del trabajo de campo.
- `Participación`: Participación estimada por la encuesta.
- `Lead`: Ventaja del primera partido más votado respecto al segundo.
- `Ganador`: El nombre del partido con más intención de voto.
- `Ventaja`: El nombre del partido con más intención de voto (Ganador) y la diferencia en puntos porcentuales respecto al segundo más votado (Lead).

## Descargar encuestas

[theelectoralreport](https://github.com/endikasatu/theelectoralreport) es una librería de R que recoge diferentes funciones enfocados al análisis y descarga de datos electorales, demográficos y encuestas.

### Cómo instalarlo

```
devtools::install_github("endikasatu/theelectoralreport")
```

### Cómo usarlo

La función para la descarga de las encuestas es `download_polls()` y admite 6 argumentos:

- `tipo`: Tipo de elección. Pueden ser "generales", "autonomicas" o " municipales".
- `ccaa`: Comunidad Autónoma donde se realiza la encuesta. Encuestas a nivel de España tendrán "**Esp.**" como CCAA.
- `prov`: Provincia donde se realiza la encuesta.
- `mun`: Municipio donde se realiza la encuesta.
- `pollster`: Encuestadora/Medio que realiza o publica la encuesta.
- `dir`: La carpeta donde se guardará la descarga.

Si no se especifican los argumentos `tipo`, `ccaa`, `prov`, `mun` o `pollster` se descargarán todas las encuestas por defecto. Estos argumentos pueden encontrar coincidencias parciales.

### Ejemplo

A continuación se detallan algunos ejemplos de uso. 

1. Para descargar las encuestas de las elecciones generales :

   ```
   download_polls(tipo = "generales", dir = "RUTA-DE-LA-CARPETA-EN-TU-ORDENADOR")
   ```

2. Para descargar las encuestas de las autonómicas en Andalucía:

   ```
   download_polls(tipo = "autonomicas", ccaa = "andalucia", dir = "RUTA-DE-LA-CARPETA-EN-TU-ORDENADOR"
   ```

3. Para descargar las encuestas para la provincia de Pontevedra en Galicia: 

   ```
   download_polls(prov = "pontevedra", dir = "RUTA-DE-LA-CARPETA-EN-TU-ORDENADOR")
   ```

4. Descargar todas las encuestas del CIS para las elecciones generales:

   ```
   download_polls(tipo = "generales", pollster = "cis", dir = "RUTA-DE-LA-CARPETA-EN-TU-ORDENADOR")
   ```

5. Descargar las encuestas municipales para la ciudad de Murcia:

   ```
   download_polls(tipo = "municipales", ccaa = "murcia", prov = "murcia", mun = "murcia",
                  dir = "RUTA-DE-LA-CARPETA-EN-TU-ORDENADOR" )
   ```

   También se puede simplificar la búsqueda de la siguiente forma:

   ```
   download_polls(tipo = "municipales", mun = "murcia", dir = "RUTA-DE-LA-CARPETA-EN-TU-ORDENADOR" )
   ```

## Licencia

Todo el material compartido en este repositorio se puede utilizar libremente. Para ello, debe realizarse una mención a TheElectoralReport y añadir el link a este repositorio.

Además, puedes consultar las condiciones de la licencia del proyecto [en este enlace](https://github.com/endikasatu/encuestas_esp/blob/main/LICENSE) o ponerte en contacto con nosotros mandando un correo a [contacto@electoralreport.com](mailto:contacto@electoralreport.com).

