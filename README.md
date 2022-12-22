# 📊 Encuestas en España

[![GitHub commit](https://img.shields.io/github/license/endikasatu/encuestas_esp)](https://github.com/endikasatu/catalunya-2021-model/blob/main/LICENSE) [![GitHub commit](https://img.shields.io/github/last-commit/endikasatu/encuestas_esp)](https://github.com/endikasatu/catalunya-2021-model/blob/main/LICENSE) 

Todas las encuestas públicas para las próximas elecciones generales, autonómicas y municipales en España recogidas por TheElectoralReport.

Consulta todas las encuestas en [TheElectoralReport](https://electoralreport.com/interactivos/encuestas/).

Creado por [Endika Nuñez](twitter.com/endikasatu).

## Archivos disponibles

Este repositorio mantiene actualizados 3 archivos .csv.

- **data/spain-polls-2019-2023.csv**: Todas las encuestas.
- **data/polls-table.html**: Tabla HTML de las encuestas. 
- **data/last-update.txt **: Fecha de la última actualización.
- **src/polls_src.csv**: URL de las encuestas en la Wikipedia.

## Variables

- `place`: Lugar donde se realiza la encuesta.
- `election_type`: Tipo de elección.
- `poll_type`: Tipo de encuesta
  - Exit poll: Encuesta a pie de urna.
  - LOREG banned: Encuesta publicada en los últimos días previos a las elecciones durante la prohibición establecida por la [Ley Orgánica de Régimen Electoral General](http://www.juntaelectoralcentral.es/cs/jec/loreg/contenido?idContenido=1509185&idLeyJunta=1&idLeyModificacion=1508162&p=1379061423059&paux=1379061423059&template=Loreg/JEC_Contenido), que dice así en su artículo 7:
  > Durante los cinco días anteriores al de la votación queda  prohibida la publicación y difusión o reproducción de sondeos  electorales por cualquier medio de comunicación.
  - Standard poll: Cualquier otra encuesta.
- `partisan`: Encuesta encargada por una formación política.
- `polling_firm`: Encuestadora encargada de realizar el sondeo y el medio que lo difunde.
- `pollster`: Encuestadora encargada de realizar el sondeo.
- `fieldwork_date`: Fecha de realización del trabajo de campo.
- `end_date`: Último día del trabajo de campo.
- `past_eday`: Fecha de las pasadas elecciones.
- `sample_size`: Número de entrevistas realizadas o tamaño de muestra.
- `turnout`: Participación estimada por la encuesta.
- `turnout_final`: Participación de las pasadas elecciones.
- `lead`: Ventaja del partido más votado respecto al segundo, en puntos porcentuales.
- `final_lead`: Ventaja del partido más votado respecto al segundo en las pasadas elecciones, en puntos porcentuales.
- `party`: Partido político o coalición
- `vote_share`: Porcentaje de voto estimado por la encuesta.
- `final_vote_share`: Porcentaje de voto de las pasadas elecciones.
- `dif_vote_share`: Diferencia, en puntos porcentuales, entre el porcentaje de voto estimado por la encuesta y el porcentaje de voto de las pasadas elecciones.
- `dif_prev_vote_share`: Diferencia, en puntos porcentuales, entre el porcentaje de voto estimado por la encuesta y la previa encuesta publicada por la misma encuestadora para las mismas elecciones.
- `winner`: Nombre del partido más votado en la encuesta.
- `winner_lead`: Nombre del partido con más votado en la encuesta  y la ventaja respecto al segundo partido, en puntos porcentuales.
- `source`: Enlace a la fuente donde se ha publicado la encuesta.
- `headline`: Titular de la fuente donde se ha publicado la encuesta.
- `url_poll`: Enlace a la fuente donde se han agregado las encuestas previamente.
- `sparkline`: Tendencia del porcentaje de voto para cada partido.

## Licencia

Todo el material compartido en este repositorio se puede utilizar libremente. Para ello, debe realizarse una mención a TheElectoralReport y añadir el link a este repositorio.

Además, puedes consultar las condiciones de la licencia del proyecto [en este enlace](https://github.com/endikasatu/encuestas_esp/blob/main/LICENSE) o ponerte en contacto con nosotros mandando un correo a [contacto@electoralreport.com](mailto:contacto@electoralreport.com).

