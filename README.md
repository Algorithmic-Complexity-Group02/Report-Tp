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
  - [Propuesta](#propuesta)
    - [Técnica y Metodología](#técnica-y-metodología)
  - [Conclusiones](#conclusiones)
  - [Bibliografía](#bibliografía)

<br><br>

## Introducción

<br>"La evolución del anime en el panorama español ha constituido un tema interesante, ya que supuso el auge de la cultura otaku" Cervantes Helena (2019). La idea de AnimePlus nace de la problematica del tiempo perdido al elegir un anime, buscar el tipo de nuestro gusto y de encontrar a nuestro autor favorito. Actualmente es muy comun tener plataformas de
Anime con una gran variedad en sus catalogos, pero es muy complicado que estas plataformas tengan un dedicado enfoque a los gustos de sus usuarios. Tambien, es sabido que a pesar de que sus bases de datos estan ya
entrenadas con los perfiles de usuarios, no logran ofrecer recomendaciones o propuestas muy claras o interesantes para la persona. AnimePlus tiene como enfoque, darle una mejor interfaz de recomendaciones y
secciones de favoritos, tanto para usuarios nuevos como antiguos. A partir de una recopilación de database de varias categorias, tipos, autores, etc. de animes, para posteriormente con la aplicacion de algoritmos
especializados, brindar una optimizacion y exactitud excelente en los catalogos. <br>

## Descripción del problema

<br>Actualmente existen plataformas de stream que ofrecen a los usuarios un catalago de anime para su consumo. La pregunta mas recurrente de estas personas que consumen anime es de no saber que otra obra poder ver una vez terminada cierta serie. Lo normal es que la app le ofresca opciones, pero el problema radica en que no son precisas estas recomendaciones. Como usuario, uno siempre desea una experecia cada vez mejor con la irterfaz de las apps, por esa razon es que el no tener recomendaciones mas precisas, un menu de usuario acoplado a los gustos del cliente y no presentar una interaccion amigable por parte de la app, es perjudicial para ambas partes y requiere un desarrollo mas enfocado en resolverlo. <br>

## Descripción del conjunto de datos

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
Cervantes Silvente, H. (2019). La repercusión del anime en la sociedad: análisis sociológico. https://hdl.handle.net/11441/131682

Shahzad, A. y Coenen, F. (2020). Efficient Distributed MST Based Clustering for Recommender Systems. 2020 International Conference on Data Mining Workshops. ICDMW. https://ieeexplore.ieee.org/document/9346360/citations?tabFilter=papers#citations
<br>

