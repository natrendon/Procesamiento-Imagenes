# Conversión RGB a CMY

## Descripción:
Script en Python para convertir imágenes del espacio de color **RGB** (Rojo, Verde, Azul) a **CMY** (Cian, Magenta, Amarillo). Ideal para fundamentos de procesamiento de imágenes y preparación para impresión.

## Requisitos:
- Python 3.7 o superior
- Librerías:
  - `opencv-python`
  - `numpy`
  - `matplotlib`

## Instalación:
``` 
pip install opencv-python numpy matplotlib

``` 

## Uso
1. Coloca tu imagen:
   
Guarda tu imagen (ejemplo: sunset.jpg) en la misma carpeta que el script.

3. Ejecuta el script:
```  
python rgb_a_cmy.py
```

3. Resultado:
   
Se mostrarán dos imágenes lado a lado:
* Del lado izquierdo la imagen original en RGB
* Del lado derecho la imagen convertida a CMY

Estructura del código
Función
* RGB2CMY(img) : Convierte imagen RGB a CMY (valores normalizados 0-1)
* cargar_imagen(ruta):	Carga imagen y la convierte de BGR a RGB
* visualizar_comparacion(rgb, cmy):	Muestra ambas imágenes para comparación

Ejemplo
``` 
from rgb_a_cmy import RGB2CMY, cargar_imagen

imagen = cargar_imagen("foto.jpg")
imagen_cmy = RGB2CMY(imagen)
```

### Notas:
* La imagen debe estar en formato RGB (3 canales)
* Los valores CMY se devuelven normalizados entre 0 y 1
* Si la imagen no se encuentra, el script mostrará un error con sugerencias

Autora: Natalia Rendón

Curso: Procesamiento de Imágenes

Fecha: Marzo 2024



# Conversión RGB a HSI

## Descripción:
Script en Python para convertir imágenes del espacio de color **RGB** (Rojo, Verde, Azul) a **HSI** (Hue, Saturation, Intensity).

## Uso
1. Coloca tu imagen:
   
Guarda tu imagen (ejemplo: sunset.jpg) en la misma carpeta que el script.

3. Ejecuta el script:
```  
python rgb_a_hsi.py
```

3. Resultado:
   
Se mostrarán dos imágenes lado a lado y tres abajo:
* Del lado izquierdo la imagen original en RGB
* Del lado derecho la imagen convertida a HSI
* Primera imagen canal Hue, segunda canal Saturation y tercera Intensity.

Estructura del código
Función
* RGB2HSI(img) :  Convierte una imagen RGB a HSI (Hue, Saturation, Intensity)(valores normalizados 0-1)
* cargar_imagen(ruta):	Carga imagen y la convierte de BGR a RGB
* visualizar_comparacion(rgb, cmy):	Muestra ambas imágenes para comparación y con solo un canal HSI

Ejemplo
``` 
from rgb_a_cmy import RGB2HSI, cargar_imagen

imagen = cargar_imagen("foto.jpg")
imagen_cmy = RGB2HSI(imagen)
```

### Notas:
* La imagen debe estar en formato RGB (3 canales)
* Los valores HSI se devuelven normalizados entre 0 y 1
* Si la imagen no se encuentra, el script mostrará un error con sugerencias

Autora: Natalia Rendón

Curso: Procesamiento de Imágenes

Fecha: Marzo 2024


# Corte de Intensidad (Intensity Slicing)

## Descripción:
Script en Python para aplicar corte de intensidad a imágenes en escala de grises. Esta técnica permite resaltar un rango específico de intensidades (niveles de gris) coloreando esos píxeles con un color definido por el usuario. Es útil para segmentación en imágenes médicas, análisis de materiales y procesamiento de imágenes satelitales.

## Requisitos:
* Python 3.7 o superior
* opencv-python
* numpy
* matplotlib

## Instalación:
``` 
pip install opencv-python numpy matplotlib
``` 
## Uso
1. Coloca tu imagen:
Guarda tu imagen (ejemplo: sunset.jpg) en la misma carpeta que el script.

2. Ejecuta el script:
``` 
python intensity_slicing.py
``` 
3. Resultado:
Se mostrarán tres visualizaciones:

a) Comparación de tres imágenes:
* Imagen original RGB
* Imagen en escala de grises
* Imagen con el corte de intensidad aplicado (rango resaltado en color)

b) Visualización con máscara:

*Imagen en escala de grises
*Máscara binaria del rango seleccionado
*Resultado final coloreado

c) Múltiples cortes:
* Imagen con tres rangos de intensidad resaltados en diferentes colores (rojo, verde, azul)


4. Estructura del código

* apply_intensity_slicing(image_path, intensity_range, color, return_mask):	Aplica corte de intensidad a una imagen en escala de grises. Resalta el rango especificado con el color indicado
* apply_multiple_slicing(image_path, ranges_colors):	Aplica múltiples cortes de intensidad con diferentes colores para cada rango
* cargar_imagen_rgb(ruta_imagen):	Carga una imagen y la convierte de BGR a RGB
* visualizar_comparacion_tres(imagen_rgb, imagen_gris, imagen_coloreada):	Muestra tres imágenes lado a lado para comparación
* visualizar_con_mascara(imagen_gris, mascara, imagen_coloreada):	Muestra la imagen original, la máscara y el resultado


## Notas:
* La imagen de entrada se convierte automáticamente a escala de grises si es a color
* El rango de intensidad debe estar entre 0 y 255
* El color debe especificarse en formato RGB con valores entre 0 y 255
* Si la imagen no se encuentra, el script mostrará un error con sugerencias

Autora:
Natalia Rendón

Curso:
Procesamiento de Imágenes

Fecha:
Abril 2024





