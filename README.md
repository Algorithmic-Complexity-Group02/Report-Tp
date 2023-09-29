<hr>

# <center>COURSE PROJECT</center>

<p align="center">
    <strong>Universidad Peruana de Ciencias Aplicadas</strong><br>
    <img src="https://upload.wikimedia.org/wikipedia/commons/f/fc/UPC_logo_transparente.png"></img><br>
    <strong>Ingeniería de Software </strong><br>
    <strong>Complejidad Algorítmica</strong><br>
    <strong>Profesor: Luis Martin Canaval Sanchez</strong><br>
    <br>INFORME DE TRABAJO FINAL - TP
</p>

<p align="center">
    <strong>Grupo 05</strong><br>
</p>

<div style="text-align:center;">
    <h3>Team Members:</h3>
    <table align="center">
        <tr>
            <th style="text-align:center;">Member</th>
            <th style="text-align:center;">Code</th>
        </tr>
        <tr>
            <td>Espinoza Quispe, Jennifer Mary</td>
            <td>U202120911</td>
        </tr>
        <tr>
            <td>Galvan Cerron, George Aldo</td>
            <td>U202116055</td>
        </tr>
        <tr>
            <td>Villanueva Torres, Ramiro Alessandro</td>
            <td>U202123714</td>
        </tr>
    </table>
</div>
<br>

<br><br>
# Índice

- [COURSE PROJECT](#course-project)
- [Índice](#índice)
  - [Introducción](#introducción)
  - [Descripción del problema](#descripción-del-problema)
  - [Descripción del conjunto de datos](#descripción-del-conjunto-de-datos)
    - [Descripción](#descripción)
      - [Primer Data Set: Anime List](#primer-data-set-anime-list)
      - [Segundo Data Set: Profile](#segundo-data-set-profile)
  - [Propuesta](#propuesta)
    - [Técnica y Metodología](#técnica-y-metodología)
  - [Conclusiones](#conclusiones)
  - [Bibliografía](#bibliografía)

<br><br>

## Introducción

"La evolución del anime en el panorama español ha sido un tema fascinante, marcando el auge de la cultura otaku" (Cervantes Helena, 2019). En este contexto, surge la idea de AnimePlus como respuesta a la problemática del tiempo perdido al seleccionar un anime, buscar el tipo que nos gusta y encontrar a nuestro autor favorito. Aunque existen numerosas plataformas de anime con extensos catálogos, es común que estas carezcan de un enfoque dedicado a los gustos individuales de los usuarios.

Una limitación notable de las plataformas existentes es que muestran contenido similar basado en su catálogo, pero no necesariamente abarcan todos los animes que existen y que podrían ajustarse a los gustos particulares de un usuario. AnimePlus aborda esta brecha al recopilar bases de datos de diversas categorías, tipos, autores, etc., de animes, garantizando así una representación más completa de la diversidad del anime.

Para lograr esto, AnimePlus emplea algoritmos avanzados como el algoritmo de Kruskal y el algoritmo BFS (Breadth-First Search). Estos algoritmos no solo consideran las preferencias generales, sino que también analizan de manera detallada los gustos específicos de cada usuario. La aplicación de estos algoritmos especializados permite una exploración exhaustiva del vasto universo del anime, asegurando recomendaciones personalizadas y precisas. La meta es crear una experiencia única para cada amante del anime al descubrir nuevas obras que se adapten a sus preferencias de manera más amplia y precisa.

</br>

## Descripción del problema

<br>En la actualidad, diversas plataformas de streaming ofrecen a los usuarios un extenso catálogo de anime para su disfrute. Sin embargo, surge una inquietud recurrente entre los consumidores de anime: la incertidumbre sobre qué obra ver después de terminar una serie en particular. Aunque las aplicaciones suelen proporcionar opciones de recomendación, el problema radica en la falta de precisión de estas sugerencias, ya que generalmente se limitan a recomendar dentro de su propio catálogo, sin abarcar la totalidad de opciones disponibles.

Como usuario, la búsqueda de una experiencia mejorada en la interfaz de las aplicaciones es constante. La ausencia de recomendaciones precisas, la falta de un menú personalizado acorde a los gustos individuales y la carencia de una interacción amigable por parte de la aplicación se convierten en obstáculos que afectan tanto a los usuarios como a las propias plataformas. Abordar esta problemática requiere un enfoque de desarrollo más centrado en solucionar estas cuestiones, mejorando así la experiencia global para ambas partes.<br>

## Descripción del conjunto de datos

Los datos que motivan nuestro análisis provienen de dos conjuntos de datos provenientes de My Anime List (MAL), una plataforma en línea dedicada a la catalogación y revisión de series de anime. Estos conjuntos de datos se han recopilado para explorar y comprender diversos aspectos relacionados con el mundo del anime y los usuarios de la plataforma.

Se ha identificado el dataset los nombres de las siguientes columnas: `uid`, `title`, `synopsis`, `genre`, `aired`, `episodes`, `members`, `popularity`, `ranked`, `score`, `img_url` y `link` teniendo un total de 19312 registros. De los cuales usaremos 2000 registros. El segundo data set con el que trabajaremos también es de My Anime List, solo que esta vez es un registro respecto al perfil del usuario con las siguientes columnas: `profile`, `gender`, `birthday`, `favorites_anime` y `link`, teniendo un total de 81729 filas de datos de las cuales usaremos 2000 datos como máximo y como mínimo 1500.

Este conjunto de datos se presta para diversas aplicaciones en inteligencia artificial, como sistemas de recomendación y análisis de sentimientos, que se centran en comprender, generar o manipular el lenguaje humano. Al explorar las calificaciones, se abre la puerta a analizar las tendencias en el mundo del anime y cómo los géneros pueden desempeñar un papel destacado en estas tendencias. Este análisis podría revelar información valiosa sobre la popularidad de ciertos géneros, los factores que influyen en la percepción de calidad de un anime y cómo evolucionan las preferencias de los usuarios a lo largo del tiempo.

### Descripción

#### Primer Data Set: Anime List

- **Origen:** Los datos comprenden un conjunto de 19,312 registros relacionados con información detallada sobre animes, como su título, género, sinopsis, fecha de emisión, número de episodios, popularidad, puntuación y más. Este conjunto se utilizará en el proyecto, centrándose en 2,000 registros para el análisis.
   - **Características Principales:**
     - 12 columnas que incluyen `uid`, `title`, `synopsis`, `genre`, `aired`, `episodes`, `members`, `popularity`, `ranked`, `score`, `img_url`, y `link`.
     - Datos relevantes para la creación de un interfaz amigable para el usuario en el frontend.
   - **Motivo de Análisis:** Este conjunto de datos es valioso para aplicaciones de inteligencia artificial, como sistemas de recomendación y análisis de sentimientos, permitiendo explorar tendencias en el mundo del anime, la influencia de géneros y factores que afectan la percepción de calidad.

En el primer conjunto de datos se pueden observar 12 columnas, las cuales serán descritas a continuación:
<div align=center>
    <img src="https://media.discordapp.net/attachments/1151952856379822130/1156893538655686667/image.png?ex=6516a091&is=65154f11&hm=ea04ac00e0e0fa119a49939f783f16fbd98294cd80f1f70bd860f58486742e7c&=&width=1620&height=198" width="90%">
</div>

| Columna       | Descripción                                          |
|---------------|------------------------------------------------------|
| Uid           | Código de identificación del anime.                  |
| Title         | Título del anime.                                    |
| Genre         | Género o géneros del anime, separados por comas.     |
| Synopsis      | Se presenta una sinopsis del anime, en inglés o en japonés.|
| Aired         | Fecha de inicio de emisión y fecha final, en formato YYYY-MM-DD.|
| Episodes      | Número de episodios del anime, o "Unknown" si no se conoce.|
| Members       | Número de miembros del anime en MyAnimeList.         |
| Popularity    | Popularidad del anime en MyAnimeList, basada en el número de miembros.|
| Ranked        | Puesto que ocupa el anime en el ranking de MyAnimeList, basado en la puntuación media.|
| Score         | Puntuación media del anime en MyAnimeList, de 0 a 10.|
| Img_url       | URL de la imagen del póster del anime.               |
| Link          | URL del anime en MyAnimeList.                        |

#### Segundo Data Set: Profile

 - **Origen:** Este conjunto de datos consta de 81,729 registros relacionados con perfiles de usuarios en MAL, incluyendo información como el nombre de usuario, género, fecha de cumpleaños, animes favoritos y enlaces a los perfiles de usuario.
   - **Características Principales:**
     - 5 columnas que incluyen `profile`, `gender`, `birthday`, `favorites_anime`, y `link`.
   - **Motivo de Análisis:** Estos datos proporcionan información sobre las preferencias y perfiles de los usuarios en la plataforma, lo que puede ser esencial para comprender las dinámicas de los usuarios y personalizar experiencias.

En el segundo conjunto de datos se pueden observar 5 columnas, las cuales serán descritas a continuación:
<div align=center>
    <img src="https://media.discordapp.net/attachments/1151952856379822130/1156894709122338897/image.png?ex=6516a1a8&is=65155028&hm=0bcc8960bd3631126051fae0e1e24f1a4ca3c8c10a84e0448cdcdeb77cefbf7b&=&width=1620&height=135" width="90%">
</div>

| Columna       | Descripción                                          |
|---------------|------------------------------------------------------|
| Profile       | El nombre de usuario del perfil.                     |
| Gender        | Género del usuario.                                  |
| Birthday      | Fecha de cumpleaños del usuario.                     |
| Favorites_anime| Lista de animes favoritos por código de anime.       |
| Link          | Link del perfil de usuario en My Anime List.        |

Cabe resaltar que tener una variedad de columnas que describen el anime es de gran utilidad porque deseamos tener una interfaz amigable para el usuario a través del front end.


<br><br>

## Propuesta

Como se menciona anteriormente, el objetivo de este proyecto es desarrollar una plataforma de recomendación de animes que utilice algoritmos de recomendación y técnicas de procesamiento de datos para proporcionar a los usuarios recomendaciones personalizadas de series y películas de animación japonesa.
<br>
### Técnica y Metodología

Para lograr este objetivo, proponemos utilizar una combinación de técnicas y algoritmos específicos que sean adecuados. Entre estos tenemos:

**Algoritmo BFS:** Puede utilizarse para encontrar animes similares a los que un usuario ha marcado como favoritos. Al explorar el grafo de conexiones, puede identificar series que son populares entre usuarios con intereses similares. De igual forma, no solo puede buscar conexiones directas, sino que también puede explorar conexiones de segundo y tercer grado, lo que significa que puede recomendar series de animación que pueden no ser favoritos directos de un usuario, pero que están relacionados con los gustos de sus conexiones.

**Algoritmo de Kruskal:** Como mencionan Shahzad y Coenen (2020), este algoritmo puede ser utilizado para optimizar la agrupación de usuarios con intereses similares, ya que el MST conectará a los usuarios que están más relacionados en función de sus gustos. Asimismo, indica que el enfoque basado en MST produce recomendaciones comparables, pero con un menor costo de almacenamiento y, por lo tanto, menor costo en tiempo de ejecución. Esto sugiere que el uso de Kruskal para generar grupos de usuarios basados en MST es una estrategia eficiente en términos de recursos.

En este sentido, consideramos que tanto BFS como Kruskal son interesantes en este proyecto de recomendación de animes. BFS permite encontrar gustos similares basados en conexiones de usuarios, mientras que Kruskal mejora  la agrupación de usuarios con gustos afines, optimiza la eficiencia y precisión de las recomendaciones.

<br>

## Conclusiones

<br><br>

## Bibliografía

<br>

- Cervantes Silvente, H. (2019). La repercusión del anime en la sociedad: análisis sociológico. https://hdl.handle.net/11441/131682

- Shahzad, A. y Coenen, F. (2020). Efficient Distributed MST Based Clustering for Recommender Systems. 2020 International Conference on Data Mining Workshops. ICDMW. https://ieeexplore.ieee.org/document/9346360/citations?tabFilter=papers#citations

- azathoth42. (2020, Octubre 31). MyAnimeList Dataset: Animes, Profiles, Reviews. Kaggle. https://www.kaggle.com/datasets/azathoth42/myanimelist 

<br>

