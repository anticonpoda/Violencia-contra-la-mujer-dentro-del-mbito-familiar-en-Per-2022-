---
title: "Trabajo"
output: html_document
date: "2024-05-11"
editor_options: 
  markdown: 
    wrap: 72
---
# Tema de investigación

En un sentido teórico, esta investigación busca reconocer distintos rasgos a nivel individual que pueden determinar el surgimiento de casos de violencia contra la mujer dentro del ámbito familiar. La exposición a una situación de violencia puede verse impulsada por diversos aspectos dentro de la identidad personal como la etnia, sexo, religión u otros, lo que explicarían a su vez el grado de vulnerabilidad para convertirse en víctimas.

En un sentido práctico, al reconocer predictores que permitan estimar la probabilidad de que ocurra un caso de violencia contra la mujer dentro del ambito familiar, esta investigación busca aportar en el diseño de políticas públicas que tengan un carácter preventivo. A partir de rangos de edad o nivel educativo se pueden elaborar políticas diferenciadas que se adapten a la realidad de las mujeres dentro de un ámbito familiar para prevenir que sucedan casos de violencia por primera vez o que ocurra una reincidencia.


# Diccionario de datos

Para el trabajo estadístico se usará la data completa de Encuesta Demográfica y de Salud Familiar (ENDES) 2022 ejecutada por el Instituto Nacional de Estadística e Informática. Link de reporte en Base de Datos Abiertos:
<https://www.datosabiertos.gob.pe/dataset/encuesta-demogr%C3%A1fica-y-de-salud-familiar-endes-2022-instituto-nacional-de-estad%C3%ADstica-e-1>
Es pertinente señalar que las personas entrevistadas han pasado por un proceso de selección y se dieron casos donde la persona seleccionada no pudo ser entrevistada porque no existían las condiciones necesarias para
garantizar la privacidad de la entrevista.

## Variable dependiente: caso de violencia contra la mujer dentro del ámbito familiar

Esta variable se encuentra distribuida en el Módulo 1637 (REC84DV) que está orientada a la maternidad y violencia familiar. Esta variable analiza la presencia y tipos de violencia experimentados por mujeres en el ámbito familiar. Incluye las siguientes subvariables:

-   D104: Violencia Emocional

    -   0 = No experimentó violencia emocional

    -   1 = Sí experimentó violencia emocional

-   D108: Violencia Sexual

    -   0 = No experimentó violencia sexual

    -   1 = Sí experimentó violencia sexual

-   D111: Cualquier resultado adverso de violencia causado por el
    esposo/compañero

    -   0 = No experimentó ningún resultado adverso causado por el
        esposo/compañero

    -   1 = Sí experimentó algún resultado adverso causado por el
        esposo/compañero

Las variables dependientes en este estudio son dicotómicas, lo que significa que cada una de ellas tiene dos posibles valores: sí y no. Posteriormente, estas variables serán combinadas en una única variable general dicotómica que representará la presencia o ausencia de cualquier tipo de violencia contra la mujer en el ámbito familiar. 

## Variables independientes:

Se encuentran en el Modulo 1631(REC0111 y REC91) de Mortalidad, Embarazo y Familia. De esta data se van a recopilar datos básicos que se usarán como variables predictoras de la violencia contra la mujere en el ambito familiar. Incluye las siguientes variables:

-   V012: Edad

    Numérica: Representa la edad de la mujer entrevistada

-   V024: Región

    Carácter: Nombre del departamento de residencia de la mujer.

-   V025: Tipo de lugar de residencia

    Numérica: Indica el tipo de lugar de residencia de la mujer.

    -   0 = Rural

    -   1 = Urbano

-   V136: Número de miembros en el hogar

    Numérica: Representa la cantidad de personas que viven en el hogar
    de la mujer.

-   V149: Logro/nivel educativo

    Numérica: Indica el último nivel educativo alcanzado por la mujer.

    -   0 = Sin Educación

    -   1 = Primaria incompleta

    -   2 = Primaria completa

    -   3 = Secundaria incompleta

    -   4 = Secundaria completa

    -   5 = Superior

-   V190: Índice de riqueza

    Numérica: Indica el nivel de riqueza del hogar al que pertenece la mujer.

    -   1 = El más pobre

    -   2 = Pobre

    -   3 = Medio

    -   4 = Rico

    -   5 = Más rico
    
-   V155: Alfabetización 

    Numérica: Indica el nivel de alfabetismo alcanzado por la mujer.

    -   0 = No puede leer

    -   1 = Puede leer solo parte de la frase

    -   2 = Puede leer la frase

    -   3 = No hay tarjeta en el idioma requerido

    -   4 = Ciega / problemas visuales 

Más adelante, esta variable será recodificada en una variable dicotómica, donde se agruparán los niveles 0, 1 y 3 como 'analfabeta', esto tendrá un valor igual a 1,  mientras que los niveles 2 y 4 se agruparán como 'no analfabeta' que tendrá el valor de 0. Esta recodificación simplificará el análisis. 

-   S119: Lengua materna

    Numérica: Indica la leguna materna de la entrevistada

    -   1= Quechua

    -   2= Aimara

    -   3= Ashaninka

    -   4= Awajún/Aguaruna

    -   5= Shipibo/Konibo

    -   6= Shawi/Chayahuita

    -   7= Matsigenka/Machiguenga

    -   8= Achuar

    -   9= Otra lengua nativa u originaria

    -   10= Castellano

    -   11= Portugués

    -   12= Otra lengua extranjera

    -   13= Es sordomuda

    -   98 = No sabe

Posteriormente, para simplificar el análisis y agrupar los datos, esta variable será recodificada en una variable dicotómica donde 1 sera igual a aquellas mujeres cuya lengua materna sea el español, y 0 a aquellas que tengan otra lengua materna distinta al español.

Todos estos datos se utilizarán para analizar y predecir la violencia contra la mujer en el ámbito familiar, considerando factores como la ubicación geográfica, nivel educativo, composición del hogar, así como el índice de riqueza del hogar.

## Variable de control

Existe una amplia literatura que sustenta el gran impacto de la etnicidad dentro de los casos de violencia contra la mujer. Por lo tanto, resulta adecuado utilizarla como variable de control en aras de poder apreciar en mayor medida el efecto de otras variables sobre los casos de violencia contra la mujer en el ámbito familiar.

-   V131: Etnicidad

    Carácter: Indica el grupo étnico al que pertenece la mujer.

    -   1= Quechua

    -   2= Aimara

    -   3= Ashaninka

    -   4= Awajún/Aguaruna

    -   5= Shipibo/Konibo

    -   6= Shawi/Chayahuita

    -   7= Matsigenka/Machiguenga

    -   8= Achuar

    -   9= Otra lengua nativa u originaria

    -   10= Castellano

    -   11= Portugués

    -   12= Otra lengua extranjera



Configuracion de la variable dependiente

```{r}
datosdep <- read.csv("REC84DVD.csv", sep = ";")
```

```{r}
vardep <- subset(datosdep, select = c("D104", "D108", "D111", "CASEID"))
```

Configuración de las variables independientes

```{r}
datosind <- read.csv("REC0111VI.csv", sep = ";")
```

```{r}
varind <- subset(datosind, select = c("V012", "V024","V025", "V131", "V149", "V136", "V190", "V155", "CASEID"))
```

```{r}
datosind1 <- read.csv("REC91.csv", sep = ";")
```

```{r}
varind1 <- subset(datosind1, select = c("S119", "CASEID"))
```

```{r}
data1 <- merge(vardep, varind, by = "CASEID", all = TRUE)

```

```{r}
datafinal <- merge(data1,varind1, by = "CASEID", all = TRUE)
```
