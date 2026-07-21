# Actividad 3

## Objetivo: ¿Qué se buscaba aprender o lograr?

Se busca que exploremos la arquitectura del computador Hack, en donde nos enfocaremos en estos conceptos:

- Las partes del computador Hack.
- El modelo de programación de la CPU.
- La diferencia entre memoria RAM y registros.
- Los tipos de instrucciones del lenguaje ensamblador.
- Cómo leo el teclado y muestro en pantalla.
- Cómo implemento un bucle.
- Cómo implemento una condición.
- ¿Qué es la ALU y qué operaciones realiza?


## Proceso: Pasos que seguiste para completar la actividad

Primeramente realice el experimento.

### **Experimento:**
Crea un archivo llamado `program.asm` y copia el código del programa anterior. Ejecuta paso a paso el programa en el **simulador** así:

- Carga el programa en el simulador.
- Antes de ejecutar cada instrucción vas a predecir qué crees que va a suceder. Es muy importante que hagas esto, de esta manera tu mismo puedes saber si estás entendiendo el programa.
- Luego, ejecuta la instrucción y observa el resultado.
- Si te equivocas, reflexiona sobre por qué tu predicción no fue correcta.

1. **Antes de ejecutar cada instrucción vas a predecir qué crees que va a suceder. Es muy importante que hagas esto, de esta manera tu mismo puedes saber si estás entendiendo el programa.**

    - `@SCREEN:` Se va a dirigir a la direccion de memoria **@16384** ya que esta es la que esta por determinado para la pantalla
    - `D=A:` Se guarda el numero de direccion de memoria, en este caso **16384**
    - `@i:` Se asigna una variable que en el IDE seria **@16** ya que la siguiente instruccion es de asignacion
    - `M=D:` Se guarda en la memoria de la direccion **@16** el numero almacenado en el registro **D**
    - `(READKEYBOARD):` Solo se nombra una etiqueta llamada **READKEYBOARD** pero esta no se ve reflejada en el IDE 
    - `@KBD:` Se dirige a la direccion asignada para el teclado
    - `D=M` Se guarda en **D** el valor almacenado en **@KBD** que depende de que tecla del teclado se presione 
    - `@KEYPRESSED:` Se dirije a la direccion de memoria dodne se encuentra guardada esta variable 
    - `D;JNE:` Si el valor es diferente a **0** saltará a la direccion de memoria dicha en la anterior instruccion, si no seguira con la siguiente instruccion
    - `@i:` Se dirije a la variable anteriormente asignada
    - `D=M:` El valor almaceando en esta lo toma el registro **D**
    - `@SCREEN:` Se dirije a la direccion asignada para la pantalla 
    - `D=D-A:` Se resta el numero de direccion de memoria **A** a el valor almacenado en el registro **D**
    - `@READKEYBOARD:` Se dirije a la direccion de memoria asignado a esta variable
    - `D;JLE:` Si el valor en **D** es menor o igual a **0** saltara a la etiqueta **READKEYBOARD**.
    - `@i:` Se dirije a la direccion de memoria asignada a esta variable.
    - `M=M-1:` Se le resta **1** al contenido de la direccion de memoria.
    - `A=M:` Se dirije a la direccion de memoria del numero que esta almacenado en la direccion de la variable **i** 
    - `M=0:` Convierte en **0** el contenido de la direccion de memoria la cual se dirigio antes
    - `@READKEYBOARD:` Nuevamente se dirige a la dirección de memoria asiganda a esta variable.
    - `0;JMP:` Sin comparar nada salta a la instruccion asignada con la etiqueta **READKEYBOARD**

    - `(KEYPRESSED):` Se asigna una etiqueta llamada **KEYPRESSED** que es para el caso en que se presione alguna tecla
    - `@i:` Se dirige a la dirección de memoria asignada a esta variable
    - `D=M:` **D** toma el contenido de esta dirección de memoria
    - `@KBD:` Se dirije a la direccion de memoria asignada al teclado
    - `D=D-A:` Se resta el numero de dirección de memoria del valor almacenado en el registro **D**
    - `@READKEYBOARD:` Se dirige nuevamente a la dirección asignada a esta variable
    - `D;JGE:` Si **D** es mayor o igual a **0** ira a la direccion de memoria llamada en la anterior instrucción.
    - `@i`
    - `A=M`
    - `M=-1`
    - `@i`
    - `M=M+1`
    - `@READKEYBOARD`
    - `0;JMP`



## Resultados: Lo que obtuviste o lograste



## Aprendizaje: Conceptos nuevos que adquiriste



## Dificultades y soluciones: Obstáculos que encontraste y cómo los superaste


## Conclusiones: Reflexión sobre la importancia de lo aprendido


