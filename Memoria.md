# Harry Popotter y la Prisionera del Data

Este proyecto comienza con la necesidad de obtener más información sobre el mundo de Harry Potter, ¿cuál es la casa más popular? ¿Cuáles son los personajes más relevantes?

## Objetivos e hipótesis

Antes de empezar con el proyecto, definí una serie de objetivos con sus respectivas hipótesis para centrarme en la búsqueda de datos correcta.

* **Objetivo_1 (principal):** "¿Qué personaje es más relevante en la saga? Teniendo en cuenta las veces que aparece, las veces que otros personajes le mencionan y proporcional al tiempo que viven."
* **Hipotesis_1 (principal):**  "Los tres personajes más relevantes serán Harry, Ron y Hermione. En ese orden. Problablemente, Dumbledore y Hagrid estén en el TOP5."
---
* **Objetivo_2:** "¿Cuál es la casa más popular entre los potterheads?"
* **Hipotesis_2:** "Gryffindor será la casa más popular seguida de Slytherin."
---
* **Objetivo_3:** "¿Cuáles son las palabras más usadas de esos personajes relevantes?"
* **Hipotesis_3:** "Las palabras destacadas serán un reflejo de su personalidad."
---
* **Objetivo_4:** "¿Cuáles son las hechizos más usados por los personajes relevantes?"
* **Hipotesis_4:** "Igual que pasaba con las palabras destacadas, los hechizos más usados serán un reflejo de su personalidad."
---
* **Objetivo_5:** "¿Coinciden las casas más populares con las casas a las que pertenecen los personajes más relevantes."
* **Hipotesis_5:** "No coincidirán salvo en el caso del trío."

## Personajes relevantes

Para analizar los personajes más relevantes, he analizado un dataset que contiene información sobre las películas, personajes y diálogos.Aquí se puede consultar el [dataset](https://github.com/sarasalguero/harrypotter/blob/main/data/Harry_Potter%20_All%20_movie%20_Chr%20Dialogs.csv) que descargué de esta página de [kaggle](https://www.kaggle.com/datasets/maricinnamon/harry-potter-movies-dataset/data)

En primer lugar, [he limpiado el dataset](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes.ipynb) para quedarme solo con las líneas de diálogo que no conteniesen NaN. Una vez está listo, es el momento de separar la información por películas para después poder analizarlos uno a uno. De este modo, obtenermos estos dataframes nuevos:
* [1_Harry_Potter_and_the_Philosophers_Stone.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/1_Harry_Potter_and_the_Philosophers_Stone.csv)
* [2_Harry_Potter_and_the_Chamber_of_Secrets.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/2_Harry_Potter_and_the_Chamber_of_Secrets.csv)
* [3_Harry_Potter_and_the_Prisoner_of_Azkaban.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/3_Harry_Potter_and_the_Prisoner_of_Azkaban.csv)
* [4_Harry_Potter_and_the_Gobelt_of_Fire.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/4_Harry_Potter_and_the_Gobelt_of_Fire.csv)
* [5_Harry_Potter_and_the_Order_of_the_Phoenix.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/5_Harry_Potter_and_the_Order_of_the_Phoenix.csv)
* [6_Harry_Potter_and_the_HalfBlood_Prince.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/6_Harry_Potter_and_the_HalfBlood_Prince.csv)
* [7_Harry_Potter_and_the_Deathly_Hallows_Part_1.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/7_Harry_Potter_and_the_Deathly_Hallows_Part_1.csv)
* [8_Harry_Potter_and_the_Deathly_Hallows_Part_2.csv](https://github.com/sarasalguero/harrypotter/blob/main/csv/8_Harry_Potter_and_the_Deathly_Hallows_Part_2.csv)

### Análisis de los personajes
He analizado todos y cada uno de esos dataframes para determinar cuáles son los 10 personajes más relevantes de cada película.

Primero contaré el proceso y, después, dejaré enlaces a los notebooks de cada película. El proceso es exactamente el mismo para cada una de ellas, solo cambia el dataframe en el que se basan.

En primer lugar, he determinado mediante una clase cuáles son los 10 personajes más relevantes de cada película basándome en las líneas de diálogo que tienen. Genera un dataframe ordenado de mayor a menor.

Una vez he detectado cuáles son los 10 personajes que más se repiten, he indagado en los diálogos para ver cuántas veces son mencionados por otros personajes (usando nombre completo, apodos, diminutivos, títulos, etc.). Esto también lo he hecho con una clase.

Una vez tenemos las dos cifras, es el momento de sumarlas y ordenar los personajes de mayor a menor.

Así, obtenemos los 10 personajes más relevantes de cada película.

A continuación, dejo enlazados los notebooks de cada una:
* [HP_1](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_1.ipynb)
* [HP_2](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_2.ipynb)
* [HP_3](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_3.ipynb)
* [HP_4](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_4.ipynb)
* [HP_5](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_5.ipynb)
* [HP_6](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_6.ipynb)
* [HP_7](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_7.ipynb)
* [HP_8](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_HP_8.ipynb)

Una vez tenemos los personajes más relevantes de las 8 películas, es el momento de determinar cuáles son los 10 personajes relevantes total. Se puede consultar el proceso en [este notebook](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/B_Personajes_z_Finalistas.ipynb)


## Casas más populares entre los potterheads

Otro de los análisis que he llevado a cabo, es determinar cuál es la casa más querida por los potterheads. Para ello, me he basado en datos obtenidos de cuatro fuentes:
* [Fuente 1](https://es.fanpop.com/clubs/harry-potter-anime/picks/results/789175/what-best-hogwarts-house)
* [Fuente 2](https://spoiler.bolavip.com/cine/Los-fans-de-Harry-Potter-eligieron-cual-es-la-peor-casa-de-Hogwarts-20211019-0024.html)
* [Fuente 3](https://en.as.com/meristation/2023/02/14/news/1676340508_316027.html)
* [Fuente 4](https://www.forbes.com/sites/paultassi/2023/02/12/here-are-the-most-popular-hogwarts-legacy-houses-ranked/?sh=aa2af37e353e)

La [fuente 3](https://en.as.com/meristation/2023/02/14/news/1676340508_316027.html) y la [fuente 4](https://www.forbes.com/sites/paultassi/2023/02/12/here-are-the-most-popular-hogwarts-legacy-houses-ranked/?sh=aa2af37e353e) son estadísticas de steam sobre Hoghwarts Legacy y no ofrecen los porcentajes sobre el cien por cien, por lo que tuve que hacer una regla de tres para determinar el porcentaje real.

De este modo, conseguí sacar los totales y así detectar el orden de las casas. Todo el trabajo se encuentra en [este notebook](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/C_Casas.ipynb).

## Palabras más usadas por los personajes destacados

Una vez tenemos el TOP10 de los personajes destacados, he querido ahondar un poco más en ellos. Para ello, he analizado los diálogos y he sacado las palabras más comunes usadas por los 5 personajes principales. Mi intención es detectar si, gracias a esto, podemos intuir su personalidad. La respuesta es que si. Se puedec consultar en este [notebook](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/D_Palabras.ipynb).

Para ello, he usado la librería "nbformat" que obvia las palabras más comunes en inglés para evitar que los mapas de palabras contengan, por ejemplo "the" como palabra más usada.

Después, he creado los mapas de palabras con "wordcloud".

## Next step: hechizos más usadas por los personajes destacados

Esta es una parte un tando "fallida" del proyecto. No he conseguido resultados esclarecedores y por eso lo voy a eliminar del proyecto final. Pero quería dejar constancia aquí del trabajo realizado.

Para esto, he usado dos datasets:
* [Harry_Potter_Spells.csv](https://github.com/sarasalguero/harrypotter/blob/main/data/Harry_Potter_Spells.csv) de [kaggle](https://www.kaggle.com/datasets/maricinnamon/harry-potter-movies-dataset/data).
* [Spells.csv](https://github.com/sarasalguero/harrypotter/blob/main/data/Spells.csv) de [kaggle]("https://www.kaggle.com/datasets/juliasays/harry-potter-spells/data).

Todo el procesoe está detallado en [este notebook](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/A_Hechizos.ipynb).

Lo primero que hice fue concatenar los dos dataframes para añadir la columna Complexity. Una vez estaba listo, cambié los NaN de la columna Effect por "No color" debido a que algunos hechizos no tienen efecto o color. De esta manera, conseguí [un dataset](https://github.com/sarasalguero/harrypotter/blob/main/csv/hechizos.csv) limpio y completo.

Para conseguir los hechizos más usadas por los personajes destacados he hecho un filtrado del diálogo del personaje en cuestión para, después, buscar los hechizos en esas líneas de diálogo. Para ello, he usado, por ejemplo, el método lower. En [este notebook](https://github.com/sarasalguero/harrypotter/blob/main/notebooks/A_Hechizos_Filtrados.ipynb) se puede consultar.

No he continuado con esto porque los resultados no me han parecido esclarecedores. Me gustaría continuar con esta parte para dejarlo cerrado.