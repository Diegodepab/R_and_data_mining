# **Introducción**

El [cáncer de mama](https://www.mayoclinic.org/es/diseases-conditions/breast-cancer/symptoms-causes/syc-20352470) es un tumor maligno que se origina en el tejido de la glándula mamaria, es el tipo más común de cáncer en mujeres a nivel mundial. Estos tumores malignos se caracterizan por tener un crecimiento descontrolado y la capacidad de extenderse a otros tejidos. Están formados por células que han acumulado alteraciones en su material genético.

La detección temprana del cáncer de mama salva vidas, mejora la calidad de vida y reduce la necesidad de tratamientos invasivos, por eso la creación de modelos predictivos es de gran utilidad. 

## **Caso de estudio**

En este trabajo se estudiará 508 muestras de pacientes recolectadas de varias fuentes, pero siguiendo las mismas pautas, cada muestra está asociada a 8 variables y la variable evento que es el estado de la respuesta patológica ([Metástasis](https://www.cancer.net/es/desplazarse-por-atenci%C3%B3n-del-c%C3%A1ncer/conceptos-b%C3%A1sicos-sobre-el-c%C3%A1ncer/%C2%BFqu%C3%A9-es-la-met%C3%A1stasis)) significa que el cáncer se ha diseminado a una parte del cuerpo distinta de donde comenzó. Cuando esto sucede, los médicos dicen que el cáncer ha hecho “metástasis”.

En esta ocasión se busca **obtener un modelo** para desplegarlo en clínica, es decir, que el oncólogo pueda usar esa ecuación obtenida en la consulta para introducir los valores de un nuevo paciente y obtener un valor entre 0 y 1 que se intepretará como **la probabilidad de que se produzca el evento**, en este caso la recidiva. En base a esta información, el clínico tomará la decisión terapeútica que considere conveniente.

## **Variables del conjunto de datos:**

Si quieres más información de como dicha variable afecta al evento puedes acceder a los links, estos llevarán a
más información: 

*Las variables de nuestro estudio:*

-   **Muestra:** Identificador de la muestra (Es un nombre único que a priori no da información) 
-   **Edad:** valor numérico con la [edad de los pacientes](https://www.cdc.gov/spanish/cancer/breast/basic_info/risk_factors.htm)  que van desde los 24 años hasta los 75 años. (más adelante habrá un apartado donde se profundiza más)
-   **REst:** [Receptores de estrógenos](https://medlineplus.gov/spanish/pruebas-de-laboratorio/pruebas-de-receptores-de-estrogeno-y-de-progesterona/)  (variable binaria con valores N para negativos y P para Positivos)
-   **RPro:** [Receptores de progesterona](https://medlineplus.gov/spanish/pruebas-de-laboratorio/pruebas-de-receptores-de-estrogeno-y-de-progesterona/) (variable binaria con valores N para negativos y P para Positivos)
-   **Her2:** [expresión de HER2](https://www.cancer.org/es/cancer/tipos/cancer-de-seno/comprension-de-un-diagnostico-de-cancer-de-seno/estado-de-her2-del-cancer-de-seno.html) (variable binaria con valores N para normales y P para Sobrexpresado)
-   **Estadio:** [Estadío de enfermedad](https://www.cancer.gov/espanol/cancer/diagnostico-estadificacion/estadificacion) (De T1 a T4)
-   **NodAfec:** [Ganglios afectados](https://thancguide.org/es/cancer-types/neck/metastatic-lymph-nodes/) (de N0 a N3)
-   **Grado:** [grado del tumor](https://www.cancer.gov/espanol/cancer/diagnostico-estadificacion/diagnostico/grado-del-tumor) (de 1 a 3)
-   **Fenotipo:** [subtipo determinado por PAM50](http://www.bio-sequence.com/pam50/) (Es decir: desde Basal, Her2, LumA, LumB y normal)

La variable **evento**:

-   **PCR:** [Estado de la respuesta patológica](https://www.clinicbarcelona.org/asistencia/enfermedades/cancer-de-mama/pruebas-y-diagnostico) (1 para pacientes en metástasis, 0 para los que no)

## **indice explicado:**
A pesar de que este trabajo no existe un guión lineal considero que a la hora de estar avanzado es bueno tener una breve descripción:  

1) _Lectura y corrección de datos:_
La fase inicial del análisis de datos en R se centra en la preparación y limpieza de los datos, abordando aspectos cruciales como la eliminación de datos erróneos, la visualización de datos perdidos, la corrección previa a la imputación, y la imputación de valores faltantes. Se procede con la eliminación de datos faltantes específicamente para el evento principal, como es el caso de los valores no disponibles para la PCR. Además, se llevan a cabo modificaciones en las variables según sea necesario para mejorar la calidad y relevancia de los datos. En particular, se exploran diversas opciones para la agrupación de edades, asegurando así una preparación adecuada para análisis posteriores.

2) _División de datos_ 
Una vez familiarizado con la base de datos y habiendo encontrado aquellas variables problematicas (variables desequilibradas principalmente), se decidirá como optar por ellas, Más adelante se analizará a detalle y mostrará la causa de guardar un dataset limpio original, un dataset eliminando variables como "Muestra" o "Her2" por problemas visto en la corrección de datos. Y la aplicación de oversampling y undersampling para comparar la mejora que proporciona ante un problema de variable evento descompensada.

3) _Validación interna de un modelo_ 
La validación interna de un modelo predictivo es un proceso mediante el cual se evalúa la capacidad predictiva del modelo utilizando los mismos datos que se utilizaron para entrenarlo. Este proceso es importante para comprender cómo se comporta el modelo en datos que ya ha visto durante el entrenamiento y para detectar posibles problemas como el sobreajuste (overfitting). Se verán multiples cantidades de métricas que nos ayuden a evaluar cúal es el mejor modelo.

4) _Búsqueda exhaustiva:_
Una vez estudiado todos los métodos considerados pertinentes para evaluar un modelo podremos descubrir cúal es el mejor modelo considerando todos los puntos anteriores. 
