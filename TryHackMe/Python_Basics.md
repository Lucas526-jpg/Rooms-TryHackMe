# Python Basics

## Introduccion

Esta sala tiene como objetivo enseñar sobre los fundamentos basicos sobre python.

## Hola mundo

Para empezar, creemos un programa sencillo que muestre un texto:  
`# This is an example comment`  
`print("Hola mundo")`

### Pregunta

En el editor de código, imprime «Hola mundo». ¿Cuál es la bandera?

Respuesta:**THM{PRINT_STATEMENTS}**

## OPERACIONES MATEMATICAS

| Operacion |	Sintaxis	| Ejemplo |
| :-- | :-- | :-- | 
| Suma	| +	| 1 + 1 = 2 |
| Resta	| -	| 5 - 1 = 4 |
| Producto	| *	| 10 * 10 = 100 |
| Division	| /	| 10 / 2 = 5 |
| Modulo	| %	| 10 % 2 = 0 |
| Potencia	| **	| 5**2 = 25 (5´2) |

### Preguntas

En el editor de código, imprime el resultado de 21 + 43. ¿Cuál es la bandera?

THM{ADDITI0N}

Imprime el resultado de 142 - 52. ¿Cuál es la bandera?

THM{SUBTRCT}

Imprime el resultado de 10 * 342. ¿Cuál es la bandera?

THM{MULTIPLICATION_PYTHON}

Imprime el resultado de 5 al cuadrado. ¿Cuál es la bandera?

**THM{EXP0N3NT_POWER}**
| Menor o igual que	| <= |

## VARIABLES Y TIPOS DE DATOS

Las variables te permiten almacenar y actualizar datos en un programa informático. Tienes un nombre de variable y almacenas datos con ese nombre.

Por ejemplo:

- comida = “helado”
- dinero = 2000

Tipo de variables(segun el dato que guardan)

- Cadena: se utiliza para combinaciones de caracteres, como letras o símbolos.
- Entero: números enteros.
- Floate: números que contienen puntos decimales o fracciones.
- Booleano: se utiliza para datos que se limitan a las opciones Verdadero o Falso.
- Lista: serie de diferentes tipos de datos almacenados en una colección.

### Preguntas

En el editor de código, crea una variable llamada altura y establece su valor inicial en 200.

`height=200`

En una nueva línea, añade 50 a la variable height.

`height=height+50`
En otra nueva línea, imprime el valor de height. ¿Cuál es la bandera que aparece?

`print(height)`

Bandera: **THM{VARIABL3S}**

## OPERACIONES LOGICAS Y BOOLEANAS

Los operadores lógicos permiten realizar asignaciones y comparaciones, y se utilizan en pruebas condicionales (como las sentencias if).

| Simbolo	| Sintaxis |
| :-- | :-- | 
| Mayor que | > |
| Menor que	| < |
| Igual a | == |
| Distinto a| != |
| Mayor o igual que	| >= |

Los operadores booleanos se utilizan para conectar y comparar relaciones entre sentencias. Al igual que en una sentencia if, las condiciones pueden ser verdaderas o falsas.

| Operación booleana | Operador | Ejemplo |
| :-- | :-- | :-- | 
| Ambas condiciones deben ser verdaderas para que la afirmación sea verdadera | AND | si x >= 5 AND x <= 100 Devuelve TRUE si x es un número entre 5 y 100 |
| Solo una condición de la afirmación tiene que ser verdadera | OR | si x == 1 OR x == 10 Devuelve TRUE si X es 1 o 10 |
| Si una condición es lo contrario de un argumento | NOT | NOT Devuelve TRUE si el valor de y es False |

## SENTENCIAS IF

El uso de sentencias if permite a los programas tomar decisiones segun alguna condicion.

Ejemplo de codigo: 

`if age < 17:
    print('No tienes la edad suficiente para conducir.')
else:
    print('Tienes la edad suficiente para conducir.')`

## BUCLES O ITERACIONES

En programación, los bucles permiten a los programas iterar y realizar acciones varias veces. Hay dos tipos de bucles: bucles for y bucles while.
