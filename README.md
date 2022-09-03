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

![ImagenTool1](https://github.com/Danacruzrui/Lab1_Daniel_Cruz_Cristhian_Pulido/blob/46bf79606f6ea5c8d254098a4e06571418085aae/Imagenes_readme/Tool1.jpeg)

Para este diseño se propone utilizar el soporte clasico del papel higenico para baños, el cual integra un resorte que se contrae de forma longitudinal, resultando ideal para esta aplicación, se realizan loscortes para facilitar la inserción del marcador y se emplea una banda elastica pequeña para limitar el movimiento axial, por ultimo se realiza un agujero en su base que posibilite la adaptación del acople macho que está en el labSIR. 
Una vez se tiene el modelo fisico se toman medidas y se crea un modelo CAD fiel a su morfologia. 


## Diseño de Workobjetc
El objeto de trabajo sobre el cual se propone trabajar son los tableros triangulares ubicados en el LabSIR, estos tableros tienen dimensiones de 308x270 vistos de frente y una inclinación que ronda los 30°, de esta forma se crea un modelo con estas dimensiones al cual se le realiza un boceto qe definirá las trayectorias a seguir.
 
![ImagenWork1](https://github.com/Danacruzrui/Lab1_Daniel_Cruz_Cristhian_Pulido/blob/46bf79606f6ea5c8d254098a4e06571418085aae/Imagenes_readme/Workk1.jpeg)
La guia de laboratorio indica que el trazo debe corresponder a las iniciales de nuestros nombres (D y C), no obstante, decidimos añadir la silueta de un animal que incluye el contorno de su cabeza, sus ojos y su nariz.
## Robot Studio 

### Creación de Herramienta 

### Creación Workobject

### Parametros de trayectoria 

### Simulación 
En la simulación se puede evidenciar el correcto seguimiento de las trayectorias contenidas en el codigo RAPID, tambien se evidencian la variación de velocidades, la zona tolerable de error y la secuencia de rutinas definida. Se define y sigue el siguiente orden: 
* Home
* Punto medio
* Contorno cara
* Contorno ojos
* Contorno nariz
* Letra D
* Letra C
* Punto Medio 
* Home
*  
![Simu1](https://github.com/Danacruzrui/Lab1_Daniel_Cruz_Cristhian_Pulido/blob/f8ca4447a73c111f65050b54a0a37405d846516a/Imagenes_readme/Simu.jpeg)
![Simu2](https://github.com/Danacruzrui/Lab1_Daniel_Cruz_Cristhian_Pulido/blob/f8ca4447a73c111f65050b54a0a37405d846516a/Imagenes_readme/Simu2.jpeg)


## Implementación 

### Posición y orientación #1
![Pose1](https://github.com/Danacruzrui/Lab1_Daniel_Cruz_Cristhian_Pulido/blob/f8ca4447a73c111f65050b54a0a37405d846516a/Imagenes_readme/Pose1.jpeg)
### Posición y orientación #2
![Pose2](https://github.com/Danacruzrui/Lab1_Daniel_Cruz_Cristhian_Pulido/blob/f8ca4447a73c111f65050b54a0a37405d846516a/Imagenes_readme/Pose2.jpeg)
## Conclusiones y aspectos por mejorar 
 * Se identifican falencias en el diseño de la herramienta, puntualmente una falta de rigidez que limite el desplazamiento axial, esto genera movimientos indeseados e imprevistos al momento de seguir la trayectoria, lo cual genera un trazo discontinuo y poco preciso
 * Se evidencia un trazo poco preciso incapaz de seguir los contornos agudos que componen el modelo original, este error esta asociado a la zona tolerable de errores la cual fue definida como z10 y era preferible un valor menor


