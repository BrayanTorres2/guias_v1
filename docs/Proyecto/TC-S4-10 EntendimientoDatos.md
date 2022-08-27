# **Entendimiento de datos**
## **Objetivo**
- Explorar y analizar fuentes de datos (entendimiento de datos) relacionadas con el proyecto del curso. 
- Inspeccionar el nivel de calidad de las fuentes de datos provistas.
- Revisar la viabilidad de implementar análisis con fuentes de datos dadas.
## **Instrucciones**

![](Img/LogoRaSA.png)

RaSA de forma conjunta con un grupo de consultores de inteligencia de negocios, ha trabajado en una especificación de los primeros análisis que quiere que usted realice. En esta primera fase, a partir de estos análisis propuestos, la empresa le ha entregado una serie de fuentes de datos y requiere que usted realice los siguientes entregables relacionados con la etapa de entendimiento de datos:

1.	**Entregable 1 - Perfilamiento de datos:** Explore las fuentes de datos compartidas y analice el resultado. 
  
2.  **Entregable 2 - Análisis de calidad de datos:** Revise las 4 dimensiones de calidad vistas en el curso en las fuentes compartidas y saque conclusiones.

3.  **Entregable 3- Conclusión del entendimiento de datos:** Valide y documente si es posible realizar los análisis solicitados, si debe hacer ajustes en la forma como han sido planteados o si requiere de información adicional para el desarrollo de los mismos. En caso de ser posible, indique explicitamente las columnas que permiten relacionar los registros de las diferentes fuentes para poder integrarlas y no olvide incluir la lista de supuestos y dudas que quedan luego de este ejercicio para que sea la empresan quien de respuesta a esas inquietudes. 

Recuerde que la exploración de los datos depende de los objetivos que tenga el proyecto de analítica. Es así como RaSA le comparte **ejemplos** de análisis que en este momento está interesado en responder:

1.	**Análisis 1:** ¿Si se tiene o se ha tenido comportamiento desleal a nivel de las aseguradoras? Está interesado en ver si dado un proveedor o grupo de proveedores si tiene o ha tenido un no comportamiento desleal? o si dado un rango de fechas se identifican proveedores con comportamientos desleales. Un comportamiento desleal corresponde a proveedores que brinden planes con el mismo tipo de beneficio cuyo valor de copago o coseguro evidencian diferencias mayores al 20% 
2.	**Análisis 2:** A lo largo del tiempo o dado un rango de años, ¿se ha logrado una cobertura total de los proveedores, cubriendo con sus plantes TODAS las áreas de servicio? ¿Han existido áreas de servicios que sean cubiertas, a nivel de planes, por  menos de dos proveedores?  
3.	**Análisis 3:** ¿Qué aeropuerto representa mayor exportación internacional en términos de carga?
4.	**Análisis 4:** ¿Identificar si hay concentraciones de planes en las áreas de servicio que no correspondan con la cantidad de habitantes del área y cuales son y en qué áreas?.
5.	**Análisis 5:** ¿Cómo han evolucionado los costos y tipos de beneficios a lo largo del tiempo para tipo de beneficio, proveedor, fecha? De tal manera que pueda identificar tipos de beneficios que han aumentado o disminuido costos.

A partir de lo anterior, los consultores de BI construyeron la siguiente tabla donde se encuentra la generalización de los ejemplos anteriores como análisis identificados y los datos requeridos para lograr los objetivos de esta tarea

| Tema analítico  | Análisis requeridos o inferidos | Categoría del análisis (*)  | Procesos de negocio | Fuentes de datos |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| Comportamiento de proveedores   | Análisis 1  | Tablero de control  |   |  |

*La categoría de análisis posibles son Tableros de control, Análisis OLAP, Aprendizaje automático, consultas SQL. En el curso solo vamos a abordar los tableros de control

** Los análisis de la tabla pueden ser agrupaciones de análisis más pequeños o se pueden extender, incluso puede que los análisis no estén completos. Es libre de proponerle nuevos análisis al negocio o complementar los de la tabla como parte de sus conclusiones. Piense en que le beneficiaría más a RaSA y en paticular a un usuario que esté interesado en este estilo de análisis.

Para esto el negocio les comenta que las fuentes de datos compartidas se agrupan en:
F1. GruposAreasdeServicio y areas de servicio  
F2. Beneficios (Tipos de beneficio y condiciones) 
F3. BeneficiosPlanes  
F4. Tablas de referencia: NivelDeRed y CondicionesDePago 

Dichos datos pueden tener errores ya que no han sido utilizados previamente para ser analizados. La empresa nos da información adicional sobre los datos:
1.	Las áreas de servicios reportadas corresponden a todas la áreas del país  
2.	Los beneficios de planes ofrecidos por diferentes proveedores no deben tener una diferencia mayor del 20%  a nivel coseguro y copago 
3.	Si hay beneficios con límite cuantitativo entonces debes tener una cantidad límite diferente de cero. 
4.	F1 y F2. Se comparte información de los años 2017 al 2021 -- Se comparten datos del 2018 – 2021 
5.	F1. Que corresponde a XXX número de grupos de servicios y YYYY números de beneficios de planes 
6.	F3. Nos comparten información de ZZZ planes del país en los años dados ( el número no coincide) 



## **Recursos requeridos**
***Datos suministrados***

Los datos los puede encontrar en la base de datos: ProyectoTransaccional del servidor que manejamos en los tutoriales. También puede encontrar el diccionario de los mismos [aquí](Diccionario%20IV.xlsx), ambos recursos requeridos para el desarrollo de esta tarea, las tablas son copias de las tablas relacionales del negocio. Son 5 tablas por lo que un estudiante del grupo se debe encargar de un grupo de fuente de datos. Las tablas compartidas son:
-	F1: GruposAreasdeServicioCopia y AreasDeServicioCopia
- F2: BeneficiosCopia
- F3: NivelDeRedCopia y CondicionesDePagoCopia
***Tecnología***

Recuerde que está el tutorial de “Entendimiento de datos”, que será de utilidad para el uso de la tecnología utilizada en esta tarea.
- JupyterLab
- Pyspark

## **Recomendaciones de los entregables**
- Recuerde incluir el significado de una fila
- Evite tener imágenes o resultados de consultas sin comentarios asociados
- Sea organizado al momento de generar el archivo a entregar

## **Preguntas o más información**
- Las preguntas que surjan en el desarrollo de esta tarea pueden registrarlas en el slack del curso.
- La forma en que se organicen y aporten al interior del grupo es fundamental para el logro del objetivo del proyecto y será evaluada en la entrega final del proyecto.
