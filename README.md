# Proyecto Aprendizaje Automático
==============================


## Objetivo del Proyecto

El objetivo del proyecto es desarrollar un modelo de aprendizaje automático que
identifique patrones en las causas de los incendios forestales y las áreas afectadas en la
provincia de Tierra del Fuego. Con este modelo, se busca predecir la probabilidad de
incendios forestales en función de variables específicas, como el tipo de vegetación y las
causas reportadas Esta información será útil para diseñar estrategias preventivas y de
manejo más efectivas, optimizando los recursos destinados a la protección ambiental.


 ## Contexto del Problema

Tierra del Fuego es una región de gran valor ecológico y cultural, con ecosistemas frágiles
y biodiversidad única. Sin embargo, en las últimas décadas, se ha observado un aumento
significativo en la frecuencia e intensidad de los incendios forestales. Estos eventos no
solo amenazan la biodiversidad local y los paisajes naturales, sino que también afectan
negativamente la economía de la provincia, especialmente en sectores como el turismo y
la producción forestal.
El análisis profundo de las causas de los incendios permitirá comprender cómo influyen
diferentes factores en la ocurrencia de estos eventos y cómo las áreas afectadas varían
según el tipo de vegetación. En esta región, los incendios pueden ser provocados tanto
por factores naturales (como rayos) como actividades humanas (fogatas, desechos mal
manejados, negligencia), lo que subraya la necesidad de identificar patrones para
prevenir futuros incendios.
El desarrollo de un modelo predictivo es fundamental para apoyar la gestión sostenible
del territorio y la protección del patrimonio natural en Tierra del Fuego.
Para guiar este proyecto, he definido las siguientes preguntas de investigación:

-¿Qué causas (naturales o humanas) se asocian con mayor frecuencia a los incendios forestales en la provincia de Tierra del Fuego? ¿Qué porcentaje de incendios forestales en TDF se atribuye a actividades humanas?

-Cuáles son los meses del año con mayor incidencia de incendios forestales en TDF?

-¿La cantidad de incendios forestales ha aumentado o disminuido en las dos últimas décadas?

-¿Cuáles son los tipos de vegetación más vulnerables a ser afectados por
incendios?

-¿Es posible predecir la ocurrencia de incendios forestales utilizando variables temporales y ambientales?
-¿Qué modelo de aprendizaje automático (Random Forest, SVM, o redes neuronales) tiene mejor desempeño al predecir la extensión de áreas afectadas (bosque nativo, pastizal, etc.)?

-¿Cuáles son los factores más importantes que influyen en la ocurrencia de incendios intencionales en la región?

-¿Es posible predecir la causa de un incendio (negligencia, intencionalidad, natural) en función de variables como el mes y tipo de cobertura vegetal?

-¿Qué tan precisos son los modelos predictivos al estimar la extensión total de hectáreas afectadas por cada tipo de vegetación?



## Descripción del dataset y origen 

### Estructura del Dataset

El dataset contiene 252 filas, cada una representando un registro mensual de incendios forestales en Tierra del Fuego entre los años 2002 y 2022. A continuación, se describen las columnas:
Año: Año en el que se registraron los incendios forestales (Numérico)
Mes: Mes del año correspondiente al registro (Categórico)
Cantidad: Total de incendios ocurridos en ese mes y año (Numérico)
Bosque nativo (has): Superficie en hectáreas de bosque nativo afectada por incendios (Numérico)
Bosque cultivado (has): Superficie en hectáreas de bosques cultivados afectada (Numérico)
Arbustal (has): Superficie de arbustos afectada en hectáreas (Numérico)
Pastizal (has): Superficie de pastizales afectadas en hectáreas (Numérico)
Negligencia (%): Porcentaje de incendios causados por negligencia (Numérico)
Intencional (%): Porcentaje de incendios causados por negligencia (Numérico)
Natural (%): Porcentaje de incendios atribuidos a causas naturales (Numérico)
Desconocida (%): Porcentaje de incendios sin causa identificada (Numérico)

### Descripción: 
Al elegir el tema del proyecto, el único dataset que encontré en la web registraba todos los datos anuales por lo que, para hacerlo mas completo, me tomé el trabajo de hacer un nuevo dataset de registro mensual compilando datos que se encuentran en [argentina.gob.ar/ambiente](https://www.argentina.gob.ar/ambiente/bosques/estadistica-forestal)

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
