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

### 1. **Motor On**
Este comando enciende los motores del brazo robótico, activando el sistema de movimiento. Es necesario para que el brazo robótico pueda moverse.

### 2. **Power Low**
Configura la potencia de los motores en un nivel bajo. Esto puede ser útil cuando se necesita que el brazo se mueva de manera precisa o a baja velocidad, como en el caso de escribir con un plumón.

### 3. **Home**
Posiciona el brazo robótico en su posición de origen o referencia. Este es el punto inicial desde donde el robot comienza su operación.

### Para escribir la letra **L**:

### 4. **Go uno**
El brazo se mueve rápidamente a la posición inicial definida como `uno`, que corresponde al punto de inicio de la letra "L".

### 5. **Move uno +Y(100)**
Mueve el brazo 100 unidades en el eje **Y** para trazar la línea vertical de la "L".

### 6. **Move uno -X(70) +Y(100)**
Este comando genera un movimiento en diagonal, bajando ligeramente en **Y** y desplazándose -70 en **X** para formar la base de la "L".

### 7. **Go Here +Z(50)**
Levanta el plumón del papel moviendo el brazo en el eje **Z** para dejar de escribir después de completar la letra.

### Para escribir la letra **I**:

### 8. **Go dos**
Mueve el brazo a la posición `dos`, que es el punto inicial para la letra "I".

### 9. **Move dos +Y(100)**
Traza una línea recta vertical de 100 unidades en el eje **Y**, dibujando la línea de la "I".

### 10. **Go Here +Z(50)**
Levanta el plumón tras completar la letra "I".

### Para escribir la letra **N**:

### 11. **Go tres**
Posiciona el brazo en `tres`, que es el inicio de la letra "N".

### 12. **Move tres -Y(100)**
Mueve el brazo 100 unidades en el eje **Y**, trazando la línea vertical de la "N".

### 13. **Move tres -X(70)**
Desplaza el brazo horizontalmente 70 unidades en el eje **X** para crear la diagonal de la "N".

### 14. **Move Here -Y(100)**
Finaliza la letra "N" moviendo el brazo hacia abajo en el eje **Y**, completando la segunda línea vertical.

### 15. **Go Here +Z(50)**
Levanta el plumón al terminar la letra.

### Para escribir la letra **O**:

### 16. **Go cuatro -X(70)**
El brazo se mueve a la posición `cuatro`, que es el punto inicial para la "O".

### 17. **Arc cuatromedio -X(70), cuatromediodos -X(70)**
Este comando traza un arco que forma la mitad de la letra "O", desplazándose en un movimiento curvo.

### 18. **Arc (cuatromedio), cuatro -X(70)**
Realiza otro movimiento en arco para completar la "O", conectando las dos mitades del círculo.

### 19. **Go Here +Z(50)**
Levanta el plumón al finalizar la letra "O".

### 20. **Motor Off**
Los motores del brazo robótico se apagan, finalizando los movimientos.

### 21. **Fend**
Este comando marca el final de la función principal, terminando la operación.

![image](https://github.com/user-attachments/assets/adea36e7-f508-46f0-a351-835a123244d4)

![Imagen de WhatsApp 2024-10-11 a las 20 52 14_88fdd55a](https://github.com/user-attachments/assets/848bd421-1ae2-4cea-ad98-36adcf1c3387)

Cabe destacar que la letra O no se pude trazar completamente ya que el pizarron se encontraba ligeramente inclinado.









