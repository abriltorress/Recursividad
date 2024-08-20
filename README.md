# Recursividad
### ¿Qué es?
la recursividad es una técnica en la que una función se llama a sí misma para resolver un problema. Esta técnica es útil para problemas que pueden dividirse en subproblemas más pequeños del mismo tipo.
### Ejemplo de recursividad en kotlin
Un ejemplo clásico de recursividad es la función que calcula el factorial de un número. El factorial de un número n (denotado como n!) es el producto de todos los enteros positivos desde 1 hasta n. La función factorial se define de la siguiente manera:

- Caso Base: factorial(0) o factorial(1) es igual a 1.
- Caso Recursivo: factorial(n) es igual a n * factorial(n - 1).

Aquí está la implementación de esta función en Kotlin:
~~~
fun factorial(n: Int): Int {
    // Caso base
    if (n <= 1) {
        return 1
    }
    // Caso recursivo
    return n * factorial(n - 1)
}

fun main() {
    println(factorial(5))  // Salida: 120
}
~~~
## Explicacion del Codigo:
### 1 | Definicion de la funcion:
~~~
fun factorial(n: Int): Int {
~~~
- **`fun`:** palabra clave en Kotlin para definir una función.
- **`factorial`:** Es el nombre de la función.
- **`(n: Int)`:** *"n"* es el parametro de la funcion y su tipo es *"Int"*. Representa el numero del cual queremos calcular el factorial.
- **`: Int`:** el tipo de retorno de la funcion es *"Int"*, que indica que la funcion devuelve un valor entero.
### 2 | Caso base: 
> Es la condición que termina la recursión, evitando que la función se llame a sí misma infinitamente. Proporciona un resultado directamente sin necesidad de hacer más llamadas recursivas.
~~~
 if (n <= 1) {
        return 1
    }
~~~
- **`if (n <= 1)`:** es una condicion que evalua si *"n"*  es igual o menor a 1 
- **`return 1`:** Si *`n`* es menor o igual a 1, la función devuelve 1.
### 3 | Caso recursivo:
> Es la parte de la función donde se llama a sí misma con un argumento modificado, acercándose al caso base. Divide el problema en subproblemas más pequeños hasta alcanzar el caso base.
~~~
return n * factorial(n - 1)
}
~~~
- **`return`:** palabra que devuelve un vaor desde la funcion.
- **`n * factorial(n - 1)`:** Aquí se multiplica *"n"* por el resultado de una llamada recursiva a la función factorial con el argumento *"n - 1"*. Esta línea representa el caso recursivo, donde la función se llama a sí misma con un valor decreciente *"(n - 1)"*, acumulando el resultado multiplicativo hasta llegar al caso base.
### 4 | Funcion main
~~~
fun main() {
    println(factorial(5))  
}
~~~
- **`fun main`:** Se define la funcion especial que se ejecuta cuando se inicia el programa
- **` println`:** funcion que imprime el valor en la consola
- **`(factorial(5))`:** llama a la funcion *`factorial`* con el argumento *`5`*. La funcion calculara el factorial de 5
## Ejecucion del codigo:
Cuando se llama a *`factorial(5)`*, el cálculo se realiza de manera recursiva:
- 1: factorial(5): Llama a factorial(4) y multiplica el resultado por 5.
- 2: factorial(4): Llama a factorial(3) y multiplica el resultado por 4.
- 3: factorial(3): Llama a factorial(2) y multiplica el resultado por 3.
- 4: factorial(2): Llama a factorial(1) y multiplica el resultado por 2.
- 5: factorial(1): Cumple con el caso base y retorna 1.
luego el resultado se multiplica hacia atras:
- factorial(2) retorna 2 × 1 = 2
- factorial(3) retorna 3 × 2 = 6
- factorial(4) retorna 4 × 6 = 24
- factorial(5) retorna 5 × 24 = 120
Finalmente, *`println`* muestra el resultado 120 en la consola.
