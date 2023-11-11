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
    <strong>Grupo 02</strong><br>
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
    - [Objetivo](#objetivo)
  - [Descripción del conjunto de datos](#descripción-del-conjunto-de-datos)
    - [Descripción](#descripción)
      - [Primer Data Set: Anime List](#primer-data-set-anime-list)
      - [Segundo Data Set: Profile](#segundo-data-set-profile)
      - [Reprentación de los nodos](#reprentación-de-los-nodos)
      - [Grafo Completo](#grafo-completo)
      - [Subgrafos](#subgrafos)
  - [Propuesta](#propuesta)
    - [Técnica y Metodología](#técnica-y-metodología)
  - [Diseño del Aplicativo](#diseño-del-aplicativo) 
    - [Diseño del Front](#diseño-del-front)
    - [Algoritmo UDFS](#algoritmo-udfs)
    - [Algoritmo BFS](#algoritmo-bfs)
  - [Conclusiones](#conclusiones)
  - [Bibliografía](#bibliografía)
  - [Anexos](#anexos)

<br><br>

## Introducción

"La evolución del anime en el panorama español ha sido un tema fascinante, marcando el auge de la cultura otaku" (Cervantes Helena, 2019). En este contexto, surge la idea de Otacopilot como respuesta a la problemática del tiempo perdido al seleccionar un anime, buscar el tipo que nos gusta y encontrar a nuestro autor favorito. Aunque existen numerosas plataformas de anime con extensos catálogos, es común que estas carezcan de un enfoque dedicado a los gustos individuales de los usuarios.

Una limitación notable de las plataformas existentes es que muestran contenido similar basado en su catálogo, pero no necesariamente abarcan todos los animes que existen y que podrían ajustarse a los gustos particulares de un usuario. Otacopilot aborda esta brecha al recopilar bases de datos de diversas categorías, tipos, autores, etc., de animes, garantizando así una representación más completa de la diversidad del anime.

Para lograr esto, Otacopilot emplea algoritmos avanzados como el algoritmo de Kruskal y el algoritmo BFS (Breadth-First Search). Estos algoritmos no solo consideran las preferencias generales, sino que también analizan de manera detallada los gustos específicos de cada usuario. La aplicación de estos algoritmos especializados permite una exploración exhaustiva del vasto universo del anime, asegurando recomendaciones personalizadas y precisas. La meta es crear una experiencia única para cada amante del anime al descubrir nuevas obras que se adapten a sus preferencias de manera más amplia y precisa.

</br>

## Descripción del problema

<br>En la actualidad, diversas plataformas de streaming ofrecen a los usuarios un extenso catálogo de anime para su disfrute. Sin embargo, existe una recurrente inquietud entre los consumidores de anime: la incertidumbre sobre qué obra ver después de terminar una serie en particular. Aunque las aplicaciones suelen proporcionar opciones de recomendación, el problema radica en la falta de precisión de estas sugerencias, ya que generalmente se limitan a recomendar dentro de su propio catálogo, sin abarcar la totalidad de opciones disponibles.

Como usuario, la búsqueda de una experiencia mejorada en la interfaz de las aplicaciones es constante. La ausencia de recomendaciones precisas, la falta de un menú personalizado acorde a los gustos individuales y la carencia de una interacción amigable por parte de la aplicación se convierten en obstáculos que afectan tanto a los usuarios como a las propias plataformas. Abordar esta problemática requiere un enfoque de desarrollo más centrado en solucionar estas cuestiones, mejorando así la experiencia global para ambas partes.<br>

### Objetivo

En ese sentido, el objetivo del proyecto es el de desarrollar un sistema de recomendación de anime que supere las limitaciones de las plataformas actuales, proporcionando a los usuarios recomendaciones precisas y personalizadas, además de una experiencia interactiva y amigable. Para lograr esto, se utilizarán diferentes algoritmos de búsqueda y recorrido de grafos para crear un sistema efectivo que mejore significativamente la experiencia de los usuarios al explorar y disfrutar del anime.


## Descripción del conjunto de datos

Los datos que motivan nuestro análisis provienen de dos conjuntos de datos provenientes de "My Anime List (MAL)", una plataforma en línea dedicada a la catalogación y revisión de series de anime. 

Se ha identificado el dataset los nombres de las siguientes columnas: `uid`, `title`, `synopsis`, `genre`, `aired`, `episodes`, `members`, `popularity`, `ranked`, `score`, `img_url` y `link` teniendo un total de 19312 registros. De los cuales usaremos 1512 registros. El segundo data set con el que trabajaremos también es de "My Anime List", solo que esta vez es un registro respecto al perfil del usuario con las siguientes columnas: `profile`, `gender`, `birthday`, `favorites_anime` y `link`, teniendo un total de 81729 filas de datos de las cuales usaremos  1538 datos.

Este conjunto de datos se presta para diversas aplicaciones en inteligencia artificial, como sistemas de recomendación y análisis de sentimientos. Al explorar las calificaciones, se abre la puerta a analizar las tendencias en el mundo del anime y cómo los géneros pueden desempeñar un papel destacado en estas tendencias. 

### Descripción

#### Primer Data Set: Anime List

- **Origen:** Los datos comprenden un conjunto de 19,312 registros relacionados con información detallada sobre animes, como su título, género, sinopsis, fecha de emisión, número de episodios, popularidad, puntuación y más. Este conjunto se utilizará en el proyecto, centrándose en 1512 registros para el análisis.
   - **Características Principales:**
     - 12 columnas que incluyen `uid`, `title`, `synopsis`, `genre`, `aired`, `episodes`, `members`, `popularity`, `ranked`, `score`, `img_url`, y `link`.
     - Datos relevantes para la creación de un interfaz amigable para el usuario en el frontend.
   - **Motivo de Análisis:** Este conjunto de datos nos     permitirá ayudar a los usuarios a encontrar animes que se ajusten a sus gustos, así como a los administradores de la plataforma a comprender mejor las tendencias y preferencias de los usuarios.

En el primer conjunto de datos se pueden observar 12 columnas, las cuales serán descritas a continuación:
<div align=center>
    <img src="https://media.discordapp.net/attachments/1151952856379822130/1156893538655686667/image.png?ex=6516a091&is=65154f11&hm=ea04ac00e0e0fa119a49939f783f16fbd98294cd80f1f70bd860f58486742e7c&=&width=1620&height=198" width="90%">
</div>

| Columna       | Descripción                                          | Tipo de Dato    |
|---------------|------------------------------------------------------|-----------------|
| Uid           | Código de identificación del anime.                  | int             |
| Title         | Título del anime.                                    | string          |
| Genre         | Género o géneros del anime, separados por comas.     | string          |
| Synopsis      | Se presenta una sinopsis del anime, en inglés o en japonés. | string  |
| Aired         | Fecha de inicio de emisión y fecha final, en formato YYYY-MM-DD. | string |
| Episodes      | Número de episodios del anime, o "Unknown" si no se conoce. | int |
| Members       | Número de miembros del anime en MyAnimeList.         | int             |
| Popularity    | Popularidad del anime en MyAnimeList, basada en el número de miembros. | int |
| Ranked        | Puesto que ocupa el anime en el ranking de MyAnimeList, basado en la puntuación media. | int |
| Score         | Puntuación media del anime en MyAnimeList, de 0 a 10. | float           |
| Img_url       | URL de la imagen del póster del anime.               | string          |
| Link          | URL del anime en MyAnimeList.                        | string          |

#### Segundo Data Set: Profile

 - **Origen:** Este conjunto de datos consta de 81,729 registros relacionados con perfiles de usuarios en MAL, incluyendo información como el nombre de usuario, género, fecha de cumpleaños, animes favoritos y enlaces a los perfiles de usuario. De los cuales usaremos 1538 registros para el análisis.
   - **Características Principales:**
     - 5 columnas que incluyen `profile`, `gender`, `birthday`, `favorites_anime`, y `link`.
   - **Motivo de Análisis:** Estos datos proporcionan información sobre las preferencias y perfiles de los usuarios en la plataforma. Esto nos permitirá comprender mejor los gustos de los usuarios y proporcionar recomendaciones más precisas.

En el segundo conjunto de datos se pueden observar 5 columnas, las cuales serán descritas a continuación:
<div align=center>
    <img src="https://media.discordapp.net/attachments/1151952856379822130/1156894709122338897/image.png?ex=6516a1a8&is=65155028&hm=0bcc8960bd3631126051fae0e1e24f1a4ca3c8c10a84e0448cdcdeb77cefbf7b&=&width=1620&height=135" width="90%">
</div>

| Columna         | Descripción                                          | Tipo de Dato    |
|-----------------|------------------------------------------------------|-----------------|
| Profile         | El nombre de usuario del perfil.                     | string          |
| Gender          | Género del usuario.                                  | string          |
| Birthday        | Fecha de cumpleaños del usuario.                     | string          |
| Favorites_anime | Lista de animes favoritos por código de anime.       | List
| Link            | Link del perfil de usuario en My Anime List.         | string          |

Cabe resaltar que tener una variedad de columnas que describen el anime es de gran utilidad porque deseamos tener una interfaz amigable para el usuario a través del front end. Por otro lado, el segundo conjunto de datos nos permite conocer los gustos de los usuarios y así poder recomendarles animes que se ajusten a sus preferencias.

#### Reprentación de los nodos
Para la representación de los nodos se ha utilizado el siguiente codigo en Python y se ha ejecutado en Google Collab

~~~Python
import pandas as pd
import matplotlib.pyplot as plt
import networkx as nx

urlProfileTest = "https://raw.githubusercontent.com/Algorithmic-Complexity-Group05/Report-Tp/feature/proposal/datasets/profiles.csv"
urlAnimeTest = "https://raw.githubusercontent.com/Algorithmic-Complexity-Group05/Report-Tp/feature/proposal/datasets/animes.csv"

df_animes = pd.read_csv(urlAnimeTest, nrows=3000)
df_usuarios = pd.read_csv(urlProfileTest, nrows=1500)

nodos = {}
bordes = []

for _, row in df_animes.iterrows():
    anime_uid = row["uid"]
    nodos[anime_uid] = {"tipo": "anime", "data": row, "title": row["title"]}

for _, row in df_usuarios.iterrows():
    user_profile = row["profile"]
    nodos[user_profile] = {"tipo": "usuario", "data": row, "nombre_perfil": user_profile}

for _, row in df_usuarios.iterrows():
    user_profile = row["profile"]
    
    favorite_animes_str = row["favorites_anime"]
    favorite_animes = [anime_id.strip(" '[]") for anime_id in favorite_animes_str.split(',')]

    for anime_uid in favorite_animes:
        if anime_uid:
            try:
                anime_uid = int(anime_uid)
                bordes.append((user_profile, anime_uid, {"tipo_interaccion": "favorito"}))
            except ValueError as e:
                print(f"Error al convertir a entero el valor '{anime_uid}' para el usuario {user_profile}: {e}")

G = {"nodos": nodos, "bordes": bordes}

G_nx = nx.DiGraph()
G_nx.add_nodes_from(G["nodos"].items())
G_nx.add_edges_from(G["bordes"])

pos = nx.spring_layout(G_nx)
labels_anime = nx.get_node_attributes(G_nx, 'title')
labels_usuario = nx.get_node_attributes(G_nx, 'nombre_perfil')

colores_nodos = ['skyblue' if data.get('tipo', 'Desconocido') == 'anime' else 'orange' for node, data in G_nx.nodes(data=True)]

G = nx.Graph(G_nx)

pos = nx.spring_layout(G, k=0.5, iterations=1000)
_, ax = plt.subplots(figsize=(20, 20))

nx.draw_networkx(G, pos, with_labels=False, node_size=10, ax=ax, node_color=colores_nodos)
ax.axis('off')

plt.show()
~~~
#### Grafo Completo

Para la representación de todos los grafos se han tomando en cuenta una parte del dataset asi como diferentes librerías de Python. Como podemos observar, en las partes laterales, no todos los nodos estan conectados, tendremos que tener en cuenta esto al momento de la realización del proyecto.

<div align=center>
    <img src="https://cdn.discordapp.com/attachments/1040019098689613875/1157714275058585650/image.png?ex=65199cf0&is=65184b70&hm=6ad7fa95313d913fbb3504b108c458553c6411b95706d978d329e3188e459b1c&" alt="Project Report"  width="70%"/>
</div>

#### Subgrafos
Asimismo, podemos ver una representación a corta escala de la conexión entre los nodos. Los nodos estarían relacionados de acuerdo a si un usuario a añadido alguna serie de anime a su lista de favoritos. 

<div align=center>
    <img src="https://media.discordapp.net/attachments/1157361311060066345/1157705079252586496/image.png?ex=65199460&is=651842e0&hm=77d1382725487bc5de890f7321e0af26b6d66ace4ee264e84e80d6305493fb32&=&width=1377&height=814" alt="Project Report"  width="70%"/>
</div>
<br>
De igual forma, podemos ver otra representación a pequeña escala de 200 nodos en total

<div align=center>
    <img src="https://media.discordapp.net/attachments/1157361311060066345/1157719105269411851/d443498a-5a45-43cd-b421-7695ff05a4db.png?ex=6519a170&is=65184ff0&hm=81e06048ac63eedb7b83cd6a3afdeadc4ea55667df76bd705e7224926d4a7e76&=&width=1218&height=814" alt="Project Report"  width="70%"/>
</div>
<br><br>

## Propuesta

Como se menciona anteriormente, el objetivo de este proyecto es desarrollar una plataforma de recomendación de animes que utilice algoritmos de recomendación y técnicas de procesamiento de datos para proporcionar a los usuarios recomendaciones personalizadas de series y películas de animación japonesa.
<br>
### Técnica y Metodología

Para lograr este objetivo, proponemos utilizar una combinación de técnicas y algoritmos específicos que sean adecuados. Entre estos tenemos:

- **Algoritmo BFS:** Puede utilizarse para encontrar animes similares a los que un usuario ha marcado como favoritos. Al explorar el grafo de conexiones, puede identificar series que son populares entre usuarios con intereses similares. De igual forma, no solo puede buscar conexiones directas, sino que también puede explorar conexiones de segundo y tercer grado, lo que significa que puede recomendar series de animación que pueden no ser favoritos directos de un usuario, pero que están relacionados con los gustos de sus conexiones.

- **Algoritmo UFDS:** La aplicación del algoritmo UFDS para gestionar relaciones entre animes se revela como una estrategia eficaz. Este algoritmo facilita la identificación y conexión de animes relacionados, permitiendo una representación eficiente de las asociaciones dentro de la base de datos.
  
- **FastAPI para Eficiencia en el Backend:** La adopción de FastAPI en el backend garantiza una ejecución rápida y eficiente de las operaciones relacionadas con la búsqueda y recomendación de animes. La capacidad de generar automáticamente documentación a través de Swagger UI simplifica la comprensión y prueba de la API, facilitando el desarrollo y la colaboración.

- **Angular para la Experiencia de Usuario:** Con su arquitectura basada en componentes, ofrece una interfaz de usuario dinámica y atractiva. La capacidad de Angular para gestionar la lógica de interfaz de usuario y presentar los resultados de las búsquedas y recomendaciones mejora significativamente la experiencia del usuario final.
  
<br>

## Diseño del Aplicativo
Nuestra app web cuenta con dos capas, estas son el "back-end" y en el "front-end", ambas trabajan en armonia para poder ejecutarse OtaCopilot, nuestro sitio web para buscar y recomendar gran variedad de Animes.
#### Diseño del Front
La primera imagen cumple con la funcion de explicar sobre la app web, nos brinda una introducción a nuestra biblioteca virtual de Anime. Para la implementación de este apartado fue necesario el uso de Html, trabajado en el entorno de Angular.
<div align=center>
    <img src="https://media.discordapp.net/attachments/1171304594312265767/1172827989172563978/image.png?ex=6561bc2e&is=654f472e&hm=ee63cdb2af4148335667c40032d25d2208772fc11ad39c7dfa0cf459a6f918c3&=&width=1306&height=614" alt="Project Report"  width="70%"/>
</div>
La segunda imagen nos muestra una barra de busqueda en la cual el usuario puede escribir el nombre del Anime deseado y en base a esta información, el software nos brindara recomendaciones a parte del Anime solicitado. Para su implementación fue necesario el adaptamiento de nuestros algoritmos de busqueda, en caso se indroduzca el nombre de algun Anime, se llamaria a un 'endpoint' que vendria a ser el back-end y este ejecutaria el algoritmo, entonces siguiendo el proceso del algoritmo nos retornaria el Anime y sus respectivas recomendaciones.
<div align=center>
    <img src="https://media.discordapp.net/attachments/1171304594312265767/1172828046017970247/image.png?ex=6561bc3c&is=654f473c&hm=2274f076434b07b4377b3ef61aa12268fc4cb7da485566cbeec91cd009c5665a&=&width=1375&height=614" alt="Project Report"  width="70%"/>
</div>
La tercera imagen es un complemento del resto de la interfaz de usuario que nos da los Anime-Card iniciales y en consecuencia de buscar un anime, tambien se aprovechara este espacio en mostrarnos las recomendaciones. 
<div align=center>
    <img src="https://media.discordapp.net/attachments/1171304594312265767/1172828139060211753/image.png?ex=6561bc52&is=654f4752&hm=ba4541215a071419fcc7cd6501a6b25dd34025dee931978b280dda5d8c752eae&=&width=1377&height=614" alt="Project Report"  width="70%"/>
</div>

#### Algoritmo UDFS
La aplicación del algoritmo UFDS para gestionar relaciones entre animes se revela como una estrategia eficaz. Este algoritmo facilita la identificación y conexión de animes relacionados, permitiendo una representación eficiente de las asociaciones dentro de la base de datos.
<div align=center>
    <img src="https://media.discordapp.net/attachments/1171304594312265767/1172828439888269312/image.png?ex=6561bc9a&is=654f479a&hm=4cc12db1bc02bd7dd5ab2aafc2491ffffebc090c7b5e7e86d95a18500c98919e&=&width=668&height=614" alt="Project Report"  width="70%"/>
</div>

#### Algoritmo BFS

La implementación de BFS como parte del conjunto de técnicas de búsqueda y recomendación en la aplicación de búsqueda de animes contribuye significativamente a ofrecer recomendaciones personalizadas y relevantes para los usuarios, mejorando así la experiencia global del usuario.

~~~
def recommend_animes_bfs(graph, source_anime_title, node_id_mapping):
    source_anime_uid = get_anime_uid(source_anime_title, graph, node_id_mapping)

    if source_anime_uid is None:
        print(f"No se encontró el anime con el título '{source_anime_title}' en el grafo.")
        return [], []

    queue = deque([(source_anime_uid, 0)])
    visited = set([source_anime_uid])
    recommended_animes = []

    while queue:
        node, distance = queue.popleft()

        if node not in node_id_mapping:
            continue

        successors = list(G_nx.successors(node_id_mapping[node]))
        if not successors:
            continue

        for neighbor in successors:

            if neighbor not in visited:
                visited.add(neighbor)
                queue.append((neighbor, distance + 1))

                node_data = G_nx.nodes[neighbor]

                if "tipo" in node_data:
                    if node_data["tipo"] == "usuario":
                        # Expandir a los animes favoritos de este usuario
                        favorites_animes = list(G_nx.successors(neighbor))
                        for anime_node in favorites_animes:
                            if anime_node not in visited:
                                visited.add(anime_node)
                                queue.append((anime_node, distance + 1))
                                recommended_animes.append((anime_node, distance + 1))

                    elif node_data["tipo"] == "anime":
                        recommended_animes.append((neighbor, distance + 1))
                else:
                    print(f"Atributo 'tipo' no encontrado para el nodo {neighbor}")
    recommended_animes.sort(key=lambda x: x[1])
    return recommended_animes
~~~


## Conclusiones
- En el presente trabajo abordamos la necesidad de personalización en las recomendaciones de anime, permitiendo a los usuarios explorar contenidos de acuerdo con sus gustos específicos.
- Nuestra idea llamada OtaCopilot utiliza algoritmos avanzados como BFS y Kruskal para proporcionar recomendaciones precisas y personalizadas.
- Buscamos permitir a los usuarios explorar el vasto universo del anime, descubriendo nuevas obras que se ajusten a sus preferencias de manera más amplia y precisa.
- Se busca proporcionar una interfaz amigable para el usuario, con una experiencia única para cada amante del anime.
  
La conjunción de FastAPI, Angular y el algoritmo UFDS proporciona una base sólida para la implementación de un sistema de recomendación personalizada. La eficiencia en el backend, la experiencia de usuario enriquecida y la capacidad del algoritmo UFDS para gestionar relaciones entre animes se combinan para ofrecer recomendaciones precisas y pertinentes basadas en las preferencias del usuario.

En resumen, la elección estratégica de estas tecnologías y algoritmos proporciona las herramientas necesarias para desarrollar una aplicación web de búsqueda de animes con capacidades avanzadas de recomendación. Esta combinación no solo optimiza la gestión de datos y la eficiencia del sistema, sino que también garantiza una experiencia de usuario envolvente y personalizada, satisfaciendo así las expectativas de los amantes del anime que buscan descubrir nuevas joyas dentro de este fascinante mundo.
<br><br>

## Bibliografía

<br>

- azathoth42. (2020, Octubre 31). MyAnimeList Dataset: Animes, Profiles, Reviews. Kaggle. https://www.kaggle.com/datasets/azathoth42/myanimelist 

- Cervantes, H. (2019). La repercusión del anime en la sociedad: análisis sociológico. https://hdl.handle.net/11441/131682

- Shahzad, A. y Coenen, F. (2020). Efficient Distributed MST Based Clustering for Recommender Systems. 2020 International Conference on Data Mining Workshops. ICDMW. https://ieeexplore.ieee.org/document/9346360/citations?tabFilter=papers#citations

<br>

## Anexos

- Link Organización GitHub: https://github.com/Algorithmic-Complexity-Group02
- Link repositorio del informe: https://github.com/Algorithmic-Complexity-Group02/Report-Tp
- Link del repositorio del dataset: https://github.com/Algorithmic-Complexity-Group02/dataset
- Link del Project: https://github.com/orgs/Algorithmic-Complexity-Group02/
projects/1/views/1
- Link del Back-end: https://github.com/Algorithmic-Complexity-Group02/OtaCopilot-API/tree/dev
- Link del front-end: https://github.com/Algorithmic-Complexity-Group02/OtaCopilot-App2/tree/dev

<div align=center>
    <img src="https://media.discordapp.net/attachments/1157361311060066345/1157705807098560562/image.png?ex=6519950d&is=6518438d&hm=f136d1592a6110a9f211d5497f4bf17ba1818831c4e7053c802458b69ceba1f1&=&width=1491&height=814" alt="Project Report"  width="80%"/>
</div>
- Evidencia Milestone 1:
  <div align=center>
    <img src="https://media.discordapp.net/attachments/1157361311060066345/1157709518042583090/image.png?ex=65199882&is=65184702&hm=0037065e9ad107c32161fbb13a89670d5a1fa2b7936d9ce004648062373dfe97&=&width=1620&height=304" alt="Project Report"  width="80%"/>
</div>

