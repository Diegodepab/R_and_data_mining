# iGraph en R

## ¿Qué es iGraph?

`igraph` es un paquete de R diseñado para la creación, manipulación y visualización de grafos. Proporciona una interfaz poderosa y flexible que permite trabajar con redes complejas de manera intuitiva. Con `igraph`, los usuarios pueden realizar análisis de redes, calcular métricas de conectividad y representar visualmente grafos de diferentes formas.

## Importancia de manejar grafos

Comprender y manejar grafos es fundamental en el análisis de datos y en varias disciplinas como la biología, la sociología y la informática. Las redes representan relaciones y conexiones entre diferentes entidades, lo que permite modelar fenómenos complejos como la propagación de enfermedades, el análisis de redes sociales, y la optimización de rutas en sistemas de transporte.

### Aplicaciones de iGraph:

1. **Análisis de Redes Sociales**: Identificar influencias y patrones en interacciones sociales.
2. **Biología de Sistemas**: Modelar interacciones entre genes, proteínas y otros biomarcadores.
3. **Ingeniería**: Optimizar sistemas de red y mejorar la eficiencia operativa.

## Ejemplos de acciones realizadas

Durante el desarrollo de este proyecto, aprendí diversas funcionalidades de `igraph`, entre las que destacan:

- **Crear Grafos**: Aprendí a crear grafos simples y complejos, especificando nodos y conexiones. Por ejemplo:

    ```r
    grafo <- graph(edges = c("a", "h", "b", "h", "c", "h", "d", "h"), directed = TRUE)
    ```

- **Configurar Estéticamente los Grafos**: Modifiqué el aspecto visual de los grafos, ajustando el tamaño de los nodos, el color y el ancho de las conexiones:

    ```r
    plot(grafo,
         vertex.size = 30,       
         vertex.color = "orange",   
         edge.color = "grey",   
         edge.width = 2)
    ```

- **Diseñar Disposiciones**: Aprendí a posicionar los nodos de manera efectiva, como colocar un nodo central y rodearlo con otros nodos:

    ```r
    layout_positions <- rbind(c(0, 0), layout_positions)  # Nodo 1 en el centro
    ```

- **Agregar Nodos y Conexiones**: Experimenté con la adición de nodos sin conexión y la creación de redes más complejas:

    ```r
    grafo <- add_vertices(grafo, 4)  # Agregar 4 nodos sin conexión
    ```

## Conclusión

El manejo de grafos es una habilidad esencial en el análisis de datos modernos. Con `igraph`, puedo construir y analizar redes de manera efectiva, permitiendo un mejor entendimiento de las relaciones en datos complejos. Este repositorio refleja el aprendizaje y la aplicación de estas técnicas en proyectos prácticos.

## Requisitos

Para utilizar el paquete `igraph`, asegúrate de tener R y el paquete instalado:

```r
install.packages("igraph")
