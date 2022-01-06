# Visión Artificial: Melanoma Clasificator

Aplicación de visión artificial para la clasificación de lunares como:
- Melanoma
- Benigno

Además, se muestra la confianza en cada una de las predicciones.

La clasificación se realiza con una red neuronal convolucional. La aplicación cuenta con una interfaz gráfica desde la que se puede seleccionar la imagen.

A continuación, se desarrolla la explicación del trabajo

## Introducción

Esta aplicación se crea para la asignatura de *Imagen médica* del Máster de Visión Artificial de la Universidad Rey Juan Carlos de Madrid. Concrétamente, tiene que clasificar imágenes de lunares como **melanoma** o como **benigno**.

Las imágenes que se han utilizado pertenecen al *dataset* [Skin Cancer: Malignant vs. Benign](https://web.archive.org/web/20201111205801/https://www.kaggle.com/fanconic/skin-cancer-malignant-vs-benign). Por comodidad, se incluyen en el repositorio.


## Diseño de la aplicación

La clasificación se realiza con una red neuronal convolucional. Se ha implementado código, tanto para la fase de entrenamiento, como para la fase de clasificación. En la fase de entrenamiento se crea un modelo de red, que será utilizado por la fase de clasificación. La aplicación almacena el mejor modelo (los mejores pesos) en la carpeta *models_melanoma*. Además, crea dos ficheros *.png* con las gráficas de precisión y pérdida del entrenamiento.

La aplicación cuenta, además, con una interfaz gráfica desde la que se puede seleccionar la imagen.


### Utilización de la aplicación

La explicación presupone que se está utilizando linux. No obstante, para otras sistemas operativos los pasos serán similares. Además, se cuenta con que se tienen correctamente instalados: *git*, *python3* y *pip*.

En el repositorio se guardan los ficheros fuentes y las imágenes, por lo que es necesario realizar una serie de pasos para poner en funcionamiento la aplicación. A continuación, se detallan todos los pasos que se ha de seguir:
1. Clonación del proyecto: `git clone https://github.com/juanluiscarrillo/CV-Melanoma-Clasificator.git`
2. Acceso a la carpeta del proyecto: `cd CV-Melanoma-Clasificator/`
3. Creación de un entorno *venv*: `python3 -m venv ./venv`
4. Activación del entorno: `source ./venv/bin/activate`
5. Instalación de dependencias: `pip3 install -r requirements.txt` 
6. Entrenamiento de la red neuronal: `python MelanomaTrainer.py --train=True`
7. Ejecución de la aplicación: `python MelanomaGUI.py`


También, es posible valorar la tasa de acierto de la aplicación sobre el conjunto de imágenes de test. Para ello habría que ejecutar: `python MelanomaTrainer.py`. 


