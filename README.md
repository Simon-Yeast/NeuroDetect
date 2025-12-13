# NeuroDetect
Modelo de detección de tumores cerebrales (Precisión del 99%). Dataset usado: https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset?resource=download
# Aplicación Web para Clasificación de Tumores Cerebrales

Este repositorio contiene un sistema de clasificación de tumores cerebrales a partir de imágenes, basado en Deep Learning, el cual se encuentra desplegado en una aplicación web desarrollada con Streamlit. El proyecto separa claramente la etapa de entrenamiento del modelo de la etapa de despliegue, permitiendo que los usuarios accedan a las predicciones sin necesidad de ejecutar código ni entrenar el modelo.

---

## Descripción del proyecto

El desarrollo del proyecto se realizó en dos etapas principales:

1. Entrenamiento y evaluación del modelo mediante un Notebook de Jupyter (.ipynb) ejecutado en Google Colab.
2. Despliegue del modelo entrenado en una aplicación web utilizando Streamlit.

El sistema permite que el usuario cargue una imagen y obtenga como resultado una predicción sobre la presencia de un tumor cerebral, el tipo de tumor identificado y el nivel de certeza asociado a dicha predicción.

---

## Entrenamiento del modelo

El entrenamiento del modelo se llevó a cabo en un entorno de Google Colab y está documentado en un archivo .ipynb. Este notebook incluye:

- Carga y preprocesamiento del conjunto de datos
- Definición de la arquitectura del modelo
- Proceso de entrenamiento y validación
- Evaluación del desempeño del modelo
- Exportación del modelo entrenado

El modelo final alcanzó una precisión aproximada del 99.5%, con resultados consistentes en los conjuntos de entrenamiento, validación y prueba.  
Una vez entrenado, el modelo se guarda y se utiliza exclusivamente para inferencia en la aplicación web.

---

## Aplicación web (Streamlit)

La aplicación web fue desarrollada con Streamlit y utiliza el modelo previamente entrenado.

A través de la interfaz web, el usuario puede:

- Cargar una imagen desde su dispositivo
- Obtener la predicción del modelo, que incluye:
  - El tipo de tumor detectado
  - La probabilidad asociada a la predicción

En esta etapa no se realiza ningún proceso de entrenamiento ni carga de datasets, ya que el modelo ya se encuentra entrenado.

Debido al uso del plan gratuito de Streamlit, la aplicación tiene fines principalmente demostrativos y académicos.

---

## Estructura del repositorio

    ├── training_notebook.ipynb   # Entrenamiento y evaluación del modelo (Google Colab)
    ├── model/                    # Archivos del modelo entrenado
    ├── app.py                    # Aplicación web desarrollada con Streamlit
    ├── requirements.txt          # Dependencias del proyecto
    └── README.md                 # Documentación del repositorio

---

## Uso

### Ejecución local

1. Clonar el repositorio:

        git clone https://github.com/usuario/nombre-del-repositorio.git

2. Instalar las dependencias:

        pip install -r requirements.txt

3. Ejecutar la aplicación:

        streamlit run app.py

---

## Aviso

Este proyecto tiene fines académicos y de investigación.  
Las predicciones generadas por el modelo no sustituyen un diagnóstico médico profesional y no deben utilizarse como herramienta clínica.
