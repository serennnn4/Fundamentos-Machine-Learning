# Fundamentos-Machine-Learning

# **Caso: Organización del laboratorio LIBIPMET**


---


### Fundamentos de Machine Learning | Proceso de Aprendizaje II
##### Por: María Fernanda León Catalán


**Problemática:** Se busca entrenar un modelo no supervisado de clustering (K-Means) para poder agrupar compuestos químicos desde las proposiciones fisicoquímicas, determinando el número óptimo de grupos. Una vez se obtenga dicho modelo, se exportará para su uso.

Dicho trabajo se presentará a través del proceso analítico EDA.


---
### **Primera fase: Recolección de datos**
##### Se importarán las librerías y después se cargará el dataset.

##Importación de librerías

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import missingno as msno


from sklearn.preprocessing import StandardScaler

from sklearn.cluster import KMeans
from sklearn.metrics import silhouette_score

import joblib
##Carga de dataset

url="https://raw.githubusercontent.com/inefable12/inteligencia_molecular/refs/heads/main/SESION_2/dataset_PA2.csv"
df=pd.read_csv(url)


##Resumen del dataset
df.head().style.set_caption("Resumen")



---


### **Segunda fase: Limpieza de datos**
##### Se evaluará la integridad y se realizará la limpieza respectiva.
