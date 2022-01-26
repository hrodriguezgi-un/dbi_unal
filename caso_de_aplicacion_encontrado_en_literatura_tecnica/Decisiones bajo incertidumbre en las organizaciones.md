# Decisiones bajo incertidumbre en las organizaciones

**Autor:** Harvey Rodriguez Gil
**Email:** hrodriguezgi@unal.edu.co

## [Optimizing urban land use allocation for planners and real estate developers](https://www.researchgate.net/publication/262454647_Optimizing_Urban_Land_Use_Allocation_for_Planners_and_Real_Estate_Developers)

### Descripción del problema

En el último siglo se ha podido ver como la población ha incrementado considerablemente: pasamos de ser 2.536 Millones de personas en el mundo a ser 7.794 Millones para el año 2020 (Ver: [World Population Prospects: Total Population by sex](https://population.un.org/wpp/DataQuery/)), lo que genera grandes retos para aquellas ciudades en donde este tipo de crecimiento ha afectado de forma directa el desarrollo de los planes de ordenamiento territorial. Y es que estos planes no solo ayudan a tener un buen uso del espacio si no a crecer de forma ordenada en el territorio disponible respetando zonas verdes y diferenciando aquellas zonas que pueden ser utilizadas con fines residenciales y las comerciales. Por otro lado, también se ha podido ver como en los últimos años la construcción de viviendas residenciales ha innovado tambien en formato vertical (edificios) creciendo en popularidad ya que permiten agrupar una mayor cantidad de personas en un espacio horizontal reducido optimizando el espacio disponible. Esto es también debido a que hemos pasado de tener una densidad de población de 19.5 personas por $km^2$ en el año 1950 a 59.9 personas por $km^2$ para el año 2020. (Ver: [World Population Prospects: Population density (persons per square km)](https://population.un.org/wpp/DataQuery/)). En la actualidad este tipo de construcciones ha ido evolucionando y ahora no solo se piensa en uso residencial, si no también en tener espacios para uso residencial y comercial con el fin de lograr una mayor rentabilidad del suelo y de lograr una mayor atracción de las personas.

### Datos requeridos

Este problema cuenta con unos stakeholders (clientes) que serán importantes para la solución objetivo del modelo. Algunos de ellos son:
- El planeador (gobierno)
- El dueño de la tierra
- El constructor o desarrollador
- Personas ambientalistas

La complejidad de asignación del uso de la tierra es debido a la gran cantidad de variables que podría llegarse a tener en cuenta. Algunas de estas  podrían ser:
- Actividad (comercial/residencial)
- Tamaño de la tierra
- Ubicación
- Actividad de los vecinos
- Tipo de construcción 
- Cantidad de pisos en la construcción
- Precio de la tierra
- Entre otros. 

Dado el tipo de problema, esto es algo que se llevaría a cabo desde la oficina de planeación territorial, por lo que la recolección de los datos requeridos se simplifica a lo que dicha oficina tiene dentro de sus bases de datos. Adicional se puede consultar fuentes de información para el caso de Colombia como [Camacol](https://camacol.co/), los cuales contienen tanto los actuales desarrollos inmobiliarios como los futuros proyectos que pueden llegar a ser utilizados de igual forma dentro de la definición del modelo.

### Descripción puntual del modelo

Como fue mencionado en la sección anterior, el problema cuenta con diferentes stakeholders, y para la definición de este solo se utilizarán dos: el planeador (gobierno) y se tomará como dueño de la tierra y el desarrollador como uno solo. La razón tomar de esta decisión es porque para el planeador lo más importante es maximizar los beneficios para la población utilizando de forma adecuada y mixta (si es del caso) la tierra asegurando un crecimiento inteligente. Por otro lado para el dueño/desarrollador lo más importante es obtener el más grande beneficio económico posible de la tierra. Dicho lo anterior el modelo deberá buscar dos soluciones, lo que se conoce como una optimización multi objetivo.

Algunas de las restricciones a tener en cuenta para el modelo son:
- Una vez definido el uso del espacio ya sea para comercial o residencial, su uso debe ser uno y solo uno.
- Los espacios de parqueaderos no debería ser considerados en la construcción del modelo

### Relación entre variables

De acuerdo a las variables planteadas a utilizar, algunas podrían llegar a tener una relación más fuerte entre ellas como lo son: tamaño de la tierra, ubicación, actividad de los vecinos; por otro lado podemos también crear relaciones entre tipo de construcción y pisos en la misma, junto con la actividad.

La revisión de este tipo de relación entre variables y el análisis de las mismas podría llevarse a cabo en un equipo que cuente con python y sus librerías para el análisis de datos.


### Consideraciones adicionales

Dado que este tipo de problemas es de tipo gubernamental, se puede encontrar una serie de problemas que pueden afectar el resultado del modelo, como lo es la frecuencia de actualización de los datos sobre el uso de la tierra que ya existe, y de la inclusión de proyectos residenciales y comerciales que ya han sido aprobados en esos datos. 

El mayor beneficio de implementar un modelo de este tipo es lograr la mejor combinación posible entre construcciones residenciales y comerciales, teniendo en cuenta aquellas zonas que deben ser protegidas (bosques, ríos, lagos) y definiendo aquellas zonas donde una construcción de tipo vertical u horizontal podría llevarse a cabo.