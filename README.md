## Recursividad
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
### Explicacion del Codigo:
- Caso Base: La función devuelve 1 cuando n es menor o igual a 1. Esto detiene la recursión.

- Caso Recursivo: La función se llama a sí misma con el argumento n - 1 y multiplica el resultado por n. Cada llamada recursiva reduce el valor de n hasta que se alcance el caso base.
