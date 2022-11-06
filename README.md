# Ejercicio-N°1
Ejercicio N°1: Frecuencias de 5 variables
## Ejercicio N°1  R -- 07/11/2022

### 1. Instalar estos Paquetes 
install.packages("tidyverse")
install.packages("dplyr")
install.packages("plyr")
install.packages("tidyr")
install.packages("mlogit")
install.packages("stargazer")
install.packages("rsq")
install.packages("sjPlot")
install.packages("dslabs")

### 1.1 Cargar desde la biblioteca estos Paquetes
library(tidyverse)
library(dplyr)
library(plyr)
library(tidyr)
library(mlogit)
library(stargazer)
library(rsq)
library(sjPlot)
library(dslabs)

## 2. Encuesta CEP
### 2.1 Link: https://www.cepchile.cl/cep/encuestas-cep/encuestas-2010-2021/estudio-nacional-de-opinion-publica-n-86-abril-mayo-de-2022

### 2.2 Importar base de datos
library(haven)
### 2.2 Importar base de datos
library(readxl)
base_86 <- read_excel("C:/Users/dmanr/Desktop/Magíster/Metodología Cuantitativa/encuesta_cep_abr_may2022/encuesta_cep_abr-may2022/base_86.xlsx")
View(base_86)

# 2.3Variable numérica
base_86[sapply(base_86, is.numeric)] <- lapply(base_86[sapply(base_86, is.numeric)], as.factor)

## 3. Análisis descriptivo

### 3.1 Frecuencias

### Variable Inicial:Región 
table(base_86$region)

### Variable 2: Identificación Religiosa
table(base_86$religion_2)

### Variable 3: Práctica Religiosa
table(base_86$religion_82)

### Variable 4: Confianza Iglesia Evangélica 
table(base_86$confianza_6_b)

### Variable 5: Confianza en el Gobierno
table(base_86$confianza_6_i)
