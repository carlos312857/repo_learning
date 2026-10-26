# ARRAYS EN JAVASCRIPT

## 1. ¿Qué son los Arrays?

Los Arrays son estructuras que permiten guardar varios datos en una sola variable, como nombres, números o frutas.

Ejemplo:

```javascript
let frutas = ["Manzana", "Pera", "Uva"];
console.log(frutas);
```

## 2. ¿Cómo funcionan los índices?

Los índices indican la posición de cada elemento. En JavaScript, empiezan desde el número 0.

```javascript
console.log(frutas[0]); // Manzana
console.log(frutas[1]); // Pera
```

## 3. Métodos principales

| Método | Función |
|---|---|
| `length` | Cuenta los elementos. |
| `push()` | Agrega un elemento al final. |
| `pop()` | Elimina el último elemento. |
| `unshift()` | Agrega un elemento al inicio. |
| `shift()` | Elimina el primer elemento. |
| `includes()` | Comprueba si existe un elemento. |
| `indexOf()` | Busca la posición de un elemento. |

## 4. Ejemplo práctico

```javascript
let videojuegos = ["Minecraft", "FIFA", "Roblox"];

videojuegos.push("Mario");
console.log(videojuegos);

videojuegos.pop();
console.log(videojuegos);

console.log(videojuegos.length);
console.log(videojuegos.includes("FIFA"));
```

En este ejemplo, creamos una lista de videojuegos, agregamos uno, eliminamos el último y consultamos cuántos elementos hay y si existe uno específico.

## 5. Ejercicio para los compañeros

Crea un Array con cinco videojuegos y realiza lo siguiente:

1. Muestra la lista en la consola.
2. Agrega un videojuego con `push()`.
3. Elimina el último con `pop()`.
4. Muestra la cantidad con `length`.
5. Comprueba si existe `"Roblox"` con `includes()`.

## 6. Conclusión

Los Arrays permiten almacenar y organizar varios datos en una sola variable. Sus métodos facilitan agregar, eliminar y buscar elementos, lo que los hace útiles al programar.





# Funciones en JavaScript

## 1. ¿Qué son las funciones?

Las funciones son bloques de código que sirven para realizar una tarea. Se pueden utilizar varias veces sin tener que repetir las mismas instrucciones.

### Ejemplo

```javascript
function saludar() {
    console.log("Hola");
}
saludar();
```

#### Explicación

Se crea una función llamada `saludar` y después se ejecuta para mostrar un mensaje.

## 2. Declarar y llamar funciones

Para crear una función se utiliza la palabra `function`, luego se escribe su nombre y se colocan paréntesis. Las instrucciones van dentro de las llaves.

### Ejemplo

```javascript
function mensaje() {
    console.log("Estoy aprendiendo JavaScript");
}
mensaje();
```

#### Explicación

La función muestra un mensaje cuando se llama.

## 3. Parámetros y argumentos

Los parámetros reciben información dentro de una función. Los argumentos son los valores que se le pasan cuando se utiliza.

### Ejemplo

```javascript
function saludar(nombre) {
    console.log("Hola " + nombre);
}
saludar("Daniel");
```

#### Explicación

`nombre` es el parámetro y `"Daniel"` es el argumento.

## 4. La instrucción return

`return` sirve para devolver un resultado que se puede utilizar en otra parte del programa.

### Ejemplo

```javascript
function sumar(a, b) {
    return a + b;
}
let resultado = sumar(5, 3);
console.log(resultado);
```

#### Resultado

```text
8
```

## 5. Funciones con varios parámetros

Una función puede recibir varios datos para realizar una operación.

### Ejemplo

```javascript
function multiplicar(a, b) {
    return a * b;
}
console.log(multiplicar(4, 5));
```

#### Resultado

```text
20
```

## 6. Funciones anónimas

Son funciones que no tienen un nombre propio y que se pueden guardar en una variable.

### Ejemplo

```javascript
const restar = function(a, b) {
    return a - b;
};
console.log(restar(10, 4));
```

#### Resultado

```text
6
```

## 7. Funciones flecha

Las funciones flecha permiten escribir funciones de una forma más corta. Se utiliza el símbolo `=>`.

### Ejemplo

```javascript
const cuadrado = numero => numero * numero;
console.log(cuadrado(5));
```

#### Resultado

```text
25
```

## 8. Alcance de las variables

El alcance indica en qué parte del código se puede utilizar una variable.

### Ejemplo

```javascript
function ejemplo() {
    let mensaje = "Hola mundo";
    console.log(mensaje);
}
ejemplo();
```

#### Explicación

La variable `mensaje` se utiliza dentro de la función `ejemplo`.

## 9. Funciones con condiciones

Las funciones pueden utilizar condiciones como `if` y `else` para tomar decisiones.

### Ejemplo

```javascript
function determinarEstado(nota) {
    if (nota >= 3) {
        return "Aprobado";
    } else {
        return "Reprobado";
    }
}
console.log(determinarEstado(4));
console.log(determinarEstado(2));
```

#### Resultado

```text
Aprobado
Reprobado
```

## 10. Funciones en nuestro proyecto

Nuestro proyecto es un sistema de calificaciones que permite ingresar tres notas, calcular el promedio y mostrar si el estudiante aprobó o reprobó.

### Función calcularPromedio

```javascript
function calcularPromedio(nota1, nota2, nota3) {
    return (nota1 + nota2 + nota3) / 3;
}
```

#### Explicación

Recibe las tres notas y devuelve el promedio.

### Función determinarEstado

```javascript
function determinarEstado(promedio) {
    if (promedio >= 3) {
        return "Aprobado";
    } else {
        return "Reprobado";
    }
}
```

#### Explicación

Comprueba si el promedio es igual o mayor que 3 para determinar el estado del estudiante.

### Función mostrarResultado

```javascript
function mostrarResultado(promedio, estado) {
    document.getElementById("resultado").innerHTML =
        "<h2>Resultados</h2>" +
        "<p>Promedio: " + promedio.toFixed(2) + "</p>" +
        "<p>Estado: " + estado + "</p>";
}
```

#### Explicación

Muestra el promedio y el estado en la página web.

### Función ejecutarEjemplo

Esta función obtiene las notas ingresadas, verific