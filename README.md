# Titulo: Clasificación de frutas en “sanas” o “mal estado” mediante imágenes usando CNN

***

## Autores:
Jorge Daniel Robles Ardila, Diego Fabián Sepúlveda Durán

***
## Banner

<img width="959" alt="Banner Proyecto I A  II" src="https://github.com/user-attachments/assets/1ac089c5-caad-432b-a765-57d59ec9fa01">

***

## Objetivo del Proyecto  
Construir un modelo de clasificación de frutas y su estado (bueno o podrido) mediante el uso de redes neuronales convolucionales (CNN), evaluando el desempeño de modelos desde cero y preentrenados.

***

## Dataset

[Enlace](https://www.kaggle.com/datasets/muhammad0subhan/fruit-and-vegetable-disease-healthy-vs-rotten)

El proyecto utiliza el dataset [**"Fruit and Vegetable Disease (Healthy vs Rotten)"**](https://www.kaggle.com/datasets/muhammad0subhan/fruit-and-vegetable-disease-healthy-vs-rotten) , que contiene imágenes clasificadas para entrenar modelos de machine learning enfocados en la detección de enfermedades en frutas y vegetales. Está organizado en 28 clases que combinan categorías de imágenes saludables y podridas para 14 tipos diferentes de frutas y vegetales. 

#### Detalles clave:
- **Número de clases:** 28 (14 tipos de frutas y vegetales, cada uno con categorías de "Saludable" y "Podrido").  
- **Formato de las imágenes:** JPEG/PNG.  
- **Uso principal:** Clasificación de imágenes y aprendizaje profundo, especialmente en tareas de detección de calidad y enfermedades en productos agrícolas.  
- **Origen:** Compilado de fuentes confiables como Kaggle y GitHub, con imágenes inspeccionadas y categorizadas manualmente.  

Para una amyor facilidad de uso e implementación, se realizó un filtrado y reducción del dataset a solo 5 tipos de frutas, cada una con igual cantidad de imagenes para "buen" y "mal" estado.

***

## Modelos de CNN utilizados 

### 1. Modelo sin preentrenar  
   Es una red convolucional construida desde cero, diseñada para procesar imágenes de 224x224 píxeles. Incluye dos bloques convolucionales con capas de normalización por lotes y dropout para evitar el sobreajuste. Termina con capas densas para producir dos salidas: una para clasificar el tipo de fruta y otra para determinar su estado (saludable o podrido). Este modelo no aprovecha conocimiento previo, por lo que requiere más tiempo de entrenamiento y datos para alcanzar buenos resultados.

![Modelo Construido draw io drawio](https://github.com/user-attachments/assets/381178d1-0068-4d7e-9894-a18feb680fff)


### 2. ResNet50  
   Utiliza un modelo preentrenado en ImageNet como base, adaptado con capas adicionales para realizar la clasificación dual. Las capas base están congeladas para evitar el sobreentrenamiento, y se utiliza una capa de agrupación global promedio antes de las salidas. ResNet50 es eficiente en extracción de características debido a su profundidad y uso de conexiones residuales, lo que resulta en alta precisión con menor tiempo de entrenamiento.

![Modelo ResNet50 drawio](https://github.com/user-attachments/assets/71c2429b-29d4-4593-b906-78e8335da2fb)


### 3. MobileNetV2  
   Es un modelo ligero y preentrenado en ImageNet, optimizado para dispositivos con recursos limitados. Similar a ResNet50, sus capas base están congeladas y se añade una capa de agrupación global promedio para ajustar las salidas. Este modelo equilibra precisión y rapidez, siendo el más rápido de los tres en tiempo de entrenamiento debido a su diseño optimizado para eficiencia computacional.  

![Modelo MobileNetV2 drawio](https://github.com/user-attachments/assets/7aeb4185-e38b-47e5-89fc-a73870d42fc6)


***

## Diapositivas 

### Link a Canva: [Enlace](https://www.canva.com/design/DAGX3mzzigo/E-F6DVekohHSC3ffuAq21g/edit?utm_content=DAGX3mzzigo&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

### Link a PDF GitHub: [Enlace]([Diapositivas I.A. 2, Entrega Final.pdf](https://github.com/Daniel121224/I.A.-2-Proyecto-Clasificacion-de-Frutas/blob/main/Diapositivas%20I.A.%202%2C%20Entrega%20Final.pdf))
