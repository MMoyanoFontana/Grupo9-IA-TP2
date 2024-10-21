# Grupo9 IA TP 2: Implementación de Redes Neuronales Artificiales para clasificación de jeroglíficos

Este proyecto contiene el código y datos correspondientes al trabajo practico N°2 de la materia Inteligencia Artificial. El objetivo del mismo es poder clasificar jeroglíficos egipcios utilizando diferentes redes neuronales, como Multi-Layer Perceptron (MLP) y Redes Neuronales Convolucionales (CNN).

## Miembros

- Bodirikyan, Cristian
- Cloarec, Anaelle
- Mahjoub, Alexandre-Skander
- Moyano Fontana, Maximiliano Iván
- Rossi, Sebastian
- Schmidt, Matias

## Contenido del Repositorio

El repositorio está estructurado de la siguiente manera:

- :framed_picture: `images/`: Contiene el dataset original, formado por los conjuntos de datos de jeroglíficos egipcios utilizados para entrenar y probar los modelos. Cada jeroglífico está representado por una imagen de 770 x 600 píxeles y un archivo XML con su posición (BoundingBox).
- :scissors: `cropped_images/`: Aca está el dataset modificado de forma que solo contenga las imagenes y que las mismas ya estén recortadas de acuerdo a su BBox.
- :wrench: `modelos_entrenados/`: Aca están los modelos de redes neuronales que fueron entrenados, para que puedan ser directamente cargados y usados.
- :chart_with_upwards_trend: `resultados/`: Directorio que contiene los gráficos e imagenes correspondientes a los resultados obtenidos con cada modelo
- :orange_book: `Grupo_9_TP_2.ipynb`: Jupyter Notebook que contiene todo el proceso realizado para preparar los datos y entrenar las distintas redes.
- :orange_book: `probar_modelos.ipynb`: Jupyter Notebook que permite probar los modelos entrenados de manera sencilla
- :scroll: `requirements.txt`: Archivo que contiene todas las dependencias necesarias para el proyecto en caso de ejecutarlo localmente.

## Uso

### Desde Google Colab
1. Ir a [Google colab](https://colab.research.google.com/)
2. Ir a Archivo > Abrir > Github
3. Copiar el Link de este repositorio ```https://github.com/MMoyanoFontana/Grupo9-IA-TP2```
4. Abrir el archivo Grupo_9_TP_2.ipynb
5. Tener en una carpeta de Google Drive al menos el directorio con las imagenes recortadas (el directorio de datos original es opcional)
6. Asegurarse de que la primera línea diga
    ```python
    use_drive = True
    ```
7. Modificar la siguiente línea de acuerdo al directorio de drive donde se subieron las imagenes
    ```python
    base_path = 'gdrive/MyDrive/IA-TP'
    ```
### Local 
1. Se necesita python 3.10.2 y un entorno donde poder ejecutar archivos .ipynb (jupyter, IDE con extensiones correspondientes)
2. Clonar el repositorio
   ```bash
   git clone https://github.com/MMoyanoFontana/Grupo9-IA-TP2.git
   cd Grupo9-IA-TP2
   ```
3.  Instalar las librerias necesarias
     ```bash
     pip install -r requirements.txt
     ```
4. Abrir el archivo Grupo_9_TP_2.ipynb 
5. Asegurarse de que la primera línea diga
   ```python
    use_drive = False
   ```
### Probar Modelos
1. Repetir los pasos para ejecutar en Colab o Local pero abriendo el notebook probar_modelos.ipynb
2. Ejecutar las primeras 3 celdas
3. Modificar la linea indicando el nombre del modelo a usar
   ``` py
   modelo_cargado = cargar_modelo("CNN_2")
   ```
4. Ejecutar la celda correspondiente según si se quiere probar el modelo con una sola imagen o varias 
   
