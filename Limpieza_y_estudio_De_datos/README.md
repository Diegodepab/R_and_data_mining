# **Introducción**

[La estimulación
ovárica](https://www.reproduccionasistida.org/estimulacion-de-la-ovulacion-en-fiv/)
es un proceso crucial en tratamientos de fertilidad, y la minería de
datos puede desempeñar un papel fundamental en su optimización. En este
contexto, exploraremos cómo los patrones ocultos en grandes conjuntos de
datos pueden proporcionarnos información valiosa sobre incrementar las
tasas de éxito, las metodologías más efectivas y otras características
relevantes.

## **Caso de estudio**

Pacientes que realizan un protocolo de doble estimulación ovárica con el
objetivo de incrementar el número de óvulos, 60 pacientes siguen la
metodología tradicional mediante el uso de [antagonistas de
GnRH](https://www.reproduccionasistida.org/antagonistas-de-gnrh/) que
inhiben la descarga de LH, a su vez 19 pacientes hacen uso de
[gestágenos](https://www.institutobernabeu.com/es/foro/gestagenos-progesterona-y-derivados/)
más económica y no hace falta inyección. La intención es ver si con uso
de gestágenos los resultados son equiparables al protocolo habitual con
antagonistas.

## **Variables del conjunto de datos:**

Si quieres más información puedes acceder a los links, estos llevarán a
más información: \> Comunes:

-   **EDAD:** [Edad de la
    paciente.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7721003/#:~:text=When%20a%20woman%20is%20younger,on%20the%20ovary%20and%20eggs.)
-   **AFC:** [Recuento de folículos
    antrales](https://www.elsevier.es/es-revista-revista-argentina-radiologia-383-articulo-recuento-foliculos-antrales-como-predictor-S0048761916301764)
-   **AMH:** [La Hormona
    Antimülleriana](https://www.reproduccionasistida.org/la-hormona-antimulleriana-amh/)
-   **FACTOR MAS:** [Presencia/ausencia factor
    masculino](https://www.elsevier.es/es-revista-medicina-familia-semergen-40-articulo-infertilidad-masculina-13089381)
-   **FACTOR FEM:** [Causa esterilidad
    femenina](https://www.mayoclinic.org/es/diseases-conditions/female-infertility/symptoms-causes/syc-20354308)
-   **BMI:** [Índice de masa
    corporal](https://www.reproduccionasistida.org/imc-embarazo/)

> Las variables usadas tanto en la primera como en la segunda
> estimulación:

-   **DIAS:** [Días de
    estimulación](https://www.reproduccionasistida.org/estimulacion-de-la-ovulacion-en-fiv/)
-   **DOSIS:** [Dosis
    suministradas](s://www.sefh.es/bibliotecavirtual/Emba/GuiaGTEIISEFHEmbarazoFebrero2022.pdf)
-   **HMG:** [Hormona folículo estimulante y hormona
    luteinizante](https://www.tuasaude.com/es/hormona-luteinizante/)
-   **N_OVO:** [Número de
    ovocitos](https://www.topdoctors.es/articulos-medicos/cuantos-ovulos-y-embriones-se-necesitan-para-conseguir-embarazo-en-ovodonacion#:~:text=Se%20necesita%20un%20n%C3%BAmero%20elevado%20de%20%C3%B3vulos%20para,se%20necesitan%2023%20%C3%B3vulos%20para%20conseguir%20un%20embarazo.)
-   **MII:** [Número de ovocitos
    maduros](https://www.reproduccionasistida.org/numero-de-ovulos-obtenido/)
-   **FERTILIZ:**
    [Fertilización](https://espanol.libretexts.org/Salud/Anatom%C3%ADa_y_Fisiolog%C3%ADa/Libro%3A_Anatom%C3%ADa_y_Fisiolog%C3%ADa_1e_(OpenStax)/Unit_6%3A_Desarrollo_Humano_y_Continuidad_de_la_Vida/28%3A_Desarrollo_y_Herencia/28.01%3A_Fertilizaci%C3%B3n)
-   **BT AA BB:** [Número de blastos de buena
    calidad](https://www.urh.es/calidad-embrionaria-que-es-un-blasto-o-blastocisto/)
-   **CONG:** [Congelación de óvulos
    (?)](https://www.nationalgeographic.es/ciencia/congelacion-ovulos-lo-que-necesitas-saber)
-   **FET:** [Procedimiento de transferencia de embriones
    congelados](https://medicinabasica.com/procedimiento-de-transferencia-de-embriones-congelados-fet)
-   **BLASTUL:** [Blastulación -llegada a blasto-
    *(evento)*](https://study.com/academy/lesson/blastulation-definition-process.html)

## **Objetivos:**

-   Identificar y discutir cualquier patrón o tendencia que sugiera una
    relación entre las características de los pacientes/tratamientos y
    los resultados de la blastulación.
-   Analizar si la respuesta en blastulación es idéntica para ambos
    grupos de tratamiento en primera y segunda estimulación.
-   Comparar la efectividad de ambos grupos de tratamientos.
-   Comprobar si las distribuciones de las variables comunes a los
    pacientes son idénticas para los dos grupos de tratamientos
    (antagonistas y gestágenos).
