# Práctica 5

## Integrantes

- Dante Mejía Silva
- Atzin Morales Alejandre

## Introducción 

En esta práctica, utilizamos el brazo robótico EPSON equipado con un plumón, con el objetivo de escribir un nombre en una superficie plana(pizarrón). Durante el ejercicio, aplicamos diversos conceptos fundamentales de la programación y control de robots, como **GO**, **MOVE** y **ARC**, para manipular el movimiento del brazo y lograr un trazado preciso de las letras.

1. **GO**: Este comando es utilizado para mover el brazo robótico de forma rápida y directa hacia una posición predeterminada sin seguir trayectorias específicas. En esta práctica, lo utilizamos para posicionar el brazo en el punto inicial antes de comenzar a escribir.

2. **MOVE**: Este comando permite movimientos controlados y lineales del brazo robótico. Se usa para trasladar el plumón de un punto a otro de manera suave y precisa, siguiendo trayectorias rectas. Durante la escritura del nombre, este comando fue clave para trazar líneas rectas que forman parte de las letras.

3. **ARC**: A diferencia de MOVE, el comando ARC se utiliza para generar movimientos curvos. En la práctica, lo empleamos para dibujar las curvas necesarias en las letras con formas redondeadas, como la “O” o la “C”, donde el plumón sigue una trayectoria circular.

La combinación de estos comandos permitió que el brazo robótico realizara trazos complejos, simulando de manera efectiva el proceso de escritura manual, con la precisión y repetibilidad propias de un sistema automatizado.

## Instrucciones

En primer lugar se eligió la palabra por escribir (LINO) y se trazó en un papel las medidas necesarias para cada letra.

![image](https://github.com/user-attachments/assets/bcd35dce-0472-4fdb-bd64-1830033fa2a8)

Posteriormente se depositaron los puntos necesarios para cada inicio de letra. 

![image](https://github.com/user-attachments/assets/25db1f5b-6268-48ea-99ae-cb3f4e3a2244)

Luego se realizó el código necesario para trazar la palabra, donde se aseguro de hacer uso de un solo punto para cada letra a excepción de las letras donde se ocuparon arcos.
```
Function main
Motor On
Power Low
Home

Go uno
Move uno +Y(100)
Move uno -X(70) +Y(100)
Go Here +Z(50)

Go dos
Move dos +Y(100)
Go Here +Z(50)

Go tres
Move tres -Y(100)
Move tres -X(70)
Move Here -Y(100)
Go Here +Z(50)

Go cuatro -X(70)
Arc cuatromedio -X(70), cuatromediodos -X(70)
Arc (cuatromedio), cuatro -X(70)
Go Here +Z(50)

Motor Off
Fend
```
Se realizó la simulación del código para asegurarnos del correcto trazo de la palabra.

![image](https://github.com/user-attachments/assets/18f53d1a-42e7-4cc2-b67f-6a026c3120f9)














