# Laboratorio 1 - Robótica Industrial
Presentado por: Daniel Alexander Cruz y Cristhian Ferney Pulido
-Danacruzrui@unal.edu.co; cfpulidog@unal.edu.co

## Resumen
En este repositorio encontrarás los archivos necesarios para desarrollar la primer practica de la asignatura de Robotica UNAL-2022-2, la cual consiste en diseñar una herramienta adaptable al Manipulador industrial ABB IRB 140 mediante la cual se pueda realizar un proceso de escritura con marcador según las trayectorias previamente definidas en el programa en RAPID. De tal forma que la rutina de RAPID será el producto de un proceso de simulación en Robot Studio en el cual se debe calibrar correctamente la herramienta y el Workobject para generar una trayectoria segura y que describa fielmente la implementación practica.

## Diseño de Herramienta 
Se busca diseñar una herramienta que cumpla con los siguientes requerimientos: 
* Sujeción rápida y segura al manipulador ABB IRB 140
* Amortiguación en el eje z (paralelo a la punta del marcador) 
* Elaboración rápida y economica 

![ImagenTool1](https://github.com/Danacruzrui/desktop-tutorial/blob/fb0f5a1244fcd00d3a96492f0f93bdab110a26ba/Imagenes_readme/Tool1.jpg)

Para este diseño se propone utilizar el soporte clasico del papel higenico para baños, el cual integra un resorte que se contrae de forma longitudinal, resultando ideal para esta aplicación, se realizan loscortes para facilitar la inserción del marcador y se emplea una banda elastica pequeña para limitar el movimiento axial, por ultimo se realiza un agujero en su base que posibilite la adaptación del acople macho que está en el labSIR. 
Una vez se tiene el modelo fisico se toman medidas y se crea un modelo CAD fiel a su morfologia. 


## Diseño de Workbjetc
![ImagenWork1](https://github.com/Danacruzrui/desktop-tutorial/blob/fb0f5a1244fcd00d3a96492f0f93bdab110a26ba/Imagenes_readme/Workk1.jpg)
## Robot Studio 

### Creación de Herramienta 

### Creación Workobject

### Parametros de trayectoria 

### Simulación 

## Implementación 
### Posición y orientación #1
### Posición y orientación #2
## Conclusiones y aspectos por mejorar 
 * Se identifican falencias en el diseño de la herramienta, puntualmente una falta de rigidez que limite el desplazamiento axial, esto genera movimientos indeseados e imprevistos al momento de seguir la trayectoria, lo cual genera un trazo discontinuo y poco preciso
 * Se evidencia un trazo poco preciso incapaz de seguir los contornos agudos que componen el modelo original, este error esta asociado a la zona tolerable de errores la cual fue definida como z10 y era preferible un valor menor


