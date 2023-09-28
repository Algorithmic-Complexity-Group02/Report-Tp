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
            <td>Nombre</td>
            <td>U</td>
        </tr>
        <tr>
            <td>Nombre</td>
            <td>U</td>
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

<br><br>

## Descripción del problema

<br><br>

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
Shahzad, A. y Coenen, F. (2020). Efficient Distributed MST Based Clustering for Recommender Systems. 2020 International Conference on Data Mining Workshops. *ICDMW*. [https://ieeexplore.ieee.org/document/9346360/citations?tabFilter=papers#citations](https://ieeexplore.ieee.org/document/9346360/citations?tabFilter=papers#citations)
<br>
