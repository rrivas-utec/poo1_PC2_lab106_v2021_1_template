# Task #PC: Práctica Calificada #2
**course:** Programación Orientada a Objetos I  
**unit:** Unidad 4 y 5  
**cmake project:** poo1_PC2_lab106_v2021_1
## Indicaciones Especificas
- El tiempo límite para la evaluación es 100 minutos.
- Cada pregunta deberá ser respondida en un archivo fuente (`.cpp`) y un archivo cabecera (`.h`) con el número de la pregunta:
    - `p1.cpp, p1.h`
    - `p2.cpp, p2.h`
    - `p3.cpp, p3.h`
- Deberás subir estos archivos directamente a [www.gradescope.com](https://www.gradescope.com) o se puede crear un `.zip` que contenga todos ellos y subirlo.

## Competencias
- Para los alumnos de la carrera de Ciencia de la Computación
    - Aplica conocimientos de computación apropiados para la solución de problemas definidos y sus requerimientos en la disciplina del programa.(nivel 2)
    - Diseña, implementa y evalúa soluciones a problemas complejos de computación.(nivel 2)
    - Crea, selecciona, adapta y aplica técnicas, recursos y herramientas modernas para la práctica de la computación y comprende sus limitaciones.(nivel 2)

- Para los alumnos de las carreras de Ingeniería
    - Capacidad para aplicar conocimientos de matemática.(nivel 2)
    - Capacidad para diseñar un sistema, un componente o un proceso para satisfacer las necesidades deseadas dentro de restricciones realistas(nivel 2)

## Question #1 - Obteniendo los indices (7 points)

Escribir y diseñar una función `obtener_indices` que retorne un vector de enteros y que permita leer un arreglo dinámico con valores enteros de tamaño `n` y un carácter `opcion` que defina las siguientes opciones:
- p par
- i impar
- r primo
```
vector<int> obtener_indices(int* arreglo,int n,char opcion);
```
La función deberá retornar un vector que contenga con los subíndices de los valores de acuerdo al parámetro opción, por ejemplo: si se elige la opción **`p`** debera generar un vector con todos los subíndices de los valores pares. Si se elige la opción **`i`** debera generar un vector con todos los subíndices de los valores impar y si se elige la opción **`r`** debera generar un vector con todos los subíndices de los valores primos.

#### Input Format

```cpp
10
1 2 10 7 6 5 11 8 4 14
p
```

#### Constraints

```cpp
- El ingreso de los valores no requiere utilizar etiquetas (std::cout)
```

#### Output Format

```cpp
1 2 4 7 8 9
```
#### Ejemplo 1
**Input**
```cpp
6
1 2 10 7 6 5
i
```
**Output**
```cpp
0 3 5
```

#### Ejemplo 2
**Input**
```cpp
12
1 2 10 7 6 5 11 31 27 2 1 9
r
```
**Output**
```cpp
1 3 5 6 7 9
```

## Question #2 - Matriz Ordenada (7 ptos)

Escribir y diseñar una función `generar_matriz_organizada` que retorne una matriz cuadrada de enteros de lado `n` y que permita leer un arreglo dinámico con valores enteros de tamaño `n x n`.

```cpp
int** generar_matriz_organizada(int* arreglo, int n);
```

La función debe tomar cada valor del arreglo y calcular su posición en la matriz usando las formulas: `i = valor/n` y `j = valor%n` y ubicar el valor en la posición correspondiente.

La matriz inicialmente debe tener sus valores en CERO.

Si la posición estuviera fuera del rango de posiciones válidas de la matriz entonces el valor se descarta.

Si anteriormente otro valor ocupará esa posición el valor deberá ser sobreescrito.

Algunos ejemplos:

#### Input Format

```cpp
3
1 2 5 7 6 5 4 8 10
```

#### Constraints

```
- El ingreso de los valores no requiere utilizar etiquetas (std::cout)
```

#### Output Format

```cpp
0 1 2
0 4 5
6 7 8
```

#### Ejemplo 1
**Input**
```cpp
2
1 2 6 5
```
**Output**
```cpp
0 1
2 0
```

#### Ejemplo 2
**Input**
```cpp
4
1 2 10 7 6 5 11 15 10 3 1 9 13 20 14 4
```
**Output**
```cpp
0  1  2  3
4  5  6  7
0  9 10 11
0 13 14 15
```

## Question #3 - Ordenada y Sin duplicados (6 points)

Escribir un programa que lea `n` valores enteros y que los almacene en un vector, modificar el vector para que solo guarde en forma ordenada los valores sin repetirlos.

#### Input Format

```cpp
8
1 2 5 7 8 5 4 8
```
#### Constraints

```
- El ingreso de los valores no requiere utilizar etiquetas (std::cout)
```

#### Output Format

```cpp
1 2 4 5 7 8
```

#### Ejemplo 1
**Input**
```cpp
20
1 2 6 5 4 12 31 20 11 2 6 3 4 5 11 59 21 22 50 11
```

#### Output Format

```cpp
1 2 3 4 5 6 11 12 20 21 22 31 50 59
```

#### Ejemplo 2
**Input**
```cpp
16
1 2 10 7 6 5 11 15 10 3 1 9 13 20 14 4
```

#### Output Format

```cpp
1 2 3 4 5 6 7 9 10 11 13 14 15 20
```
