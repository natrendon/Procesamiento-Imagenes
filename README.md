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
