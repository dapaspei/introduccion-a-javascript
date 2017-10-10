# Introducción a Javascript
+++
## Lenguaje de programación compatible con todos los navegadores. Se ejecuta en el navegador, no en el servidor.
+++
## Orientado a objetos
+++
## Lenguaje NO tipado
+++
## Intepretado (navegador)
+++
## Extensión **.js**
+++
## Ejemplo de sintaxis:
```
function sumar(num1, num2) {	
	return num1 + num2;
}

sumar (3, 2);
```
+++
## Javascript en Servidor 
- Phonegap / Apache Cordova
- Unity3D
- Televisiones: Netflix, Firefox OS, 

---
# Ejecución de Javascript
+++
El código javascript se ejecuta entre las etiquetas:
```
<script>
Mi código 
</script>
```
+++
Se puede, pero a partir de html5, NO hace falta poner:
```
<script **type=“text/javascript”**>
...
```
+++
Todos los navegadores tienen "consola" o "terminal", para poner *comandos* y ejecutar código javascript y comprobar qué hace nuestro programa.
+++
```
<script>
	console.log(“Hola a tod@s!”);
</script>
```
---
# Variables
## Definición
### Es un elemento que contiene un valor. Y ese valor puede variar.
+++
# Sintaxis:
```
nombre = “Dani”;
numero = 10;
otroNumero = 1.0;
```
+++
# Comprobar el contenido de una variable
```
<script>
nombre = "Dani";
console.log(nombre);
</script>
```
+++
# Tipado débil 
(si no lo entiendes, no te preocupes)
+++
# Tipos de datos
## Cadenas de caracteres “Strings” (“Dani”)
## Números enteros “integer” (10)
## Números con decimales “float” (1.0)
## Valores lógicos “bolean” (true/false)
+++
# Comentarios
```
// Esto es un comentario de una línea
/* 
	Esto es un
	comentario de
	varias líneas
*/
```
+++
# Operaciones Aritméticas
```
<script>
edad = 30;
total = edad + 9;    // Suma
// total = edad - 9; // Resta
// total = edad * 2; // Multiplicación
// total = edad / 2; // División
console.log(total);
</script>
```
+++
# Unir cadenas (Concatenación)
```
<script>
nombre = "Dani";
apellido = "Pastor";
nombreCompleto = nombre + " " + apellido;
console.log(nombreCompleto);
</script>
```
---

# Funciones Estructurales
## Funciones mínimas para crear otras funciones
+++
### Función IF (1)
```
<script>
nombre = "Dani";
// Se pregunta y devuelve "true" o "false"
if (nombre == "Dani") { 
	console.log("Hola: " + nombre);
} else {
	console.log("No sé quien eres :-( " + nombre);
}
</script>
```
+++
### Función IF (2)
```
<script>
edad = 30;
// Si la variable edad es menor que 35 entra en el primer bloque
if (edad < 35) { 
	console.log("Tienes menos de 35 años");
} else {
	console.log("Tienes más de 35 años");
}
</script>
```
+++
### Función IF (3)
```
<script>
admin = true;
// Si admin es true, entrará en el primer bloque
if (admin) { 
	console.log("Eres el administrado!");
} else {
	console.log("No eres el administrador");
}
</script>
```
+++
### Función IF (4)
```
<script>
// Varias sentencias IF - AND
nombre = "Dani";
admin = false;
// true && false
if (nombre == "Dani" && admin) { 
	console.log("Hola: " + nombre +", eres el administrador!");
} else {
	console.log("No eres administrador: " + nombre);
}
</script>
```
+++
### Función IF (5)
```
<script>
// Varias sentencias IF - OR
nombre = "Dani";
admin = false;
// true || false
if (nombre == "Dani" || admin) { 
	console.log("Hola: " + nombre +", eres el administrador!");
} else {
	console.log("No eres administrador: " + nombre);
}
</script>
```
+++
### Función SWITCH
```
<script>
nombre = "Dani";
// Varias condiciones a la vez
switch (nombre) {
	case "Dani":
		console.log("El usuario es Dani.");
		break; // se sale del switch
	case "John":
		console.log("El usuario es John.");
		break;
	default:
	  console.log("Usuario desconocido.");

}
</script>
```
+++
### Función FOR
```
<script>
nombre = "Dani";
// bucles: repetir el contenido varias veces

// inicializa una variable llamada 'cont' al valor 0
// pregunta si el valor es menor que 5 (como un 'if')
// suma 1 al valor actual de 'cont'
for (var cont = 0; cont < 5; cont++) {
	  console.log("El valor del contador es: " + cont);
}
</script>
```
---
# Función:
## Es un conjunto de acciones y comandos que se ejecutan bajo un nombre.
+++
```
<script>
numero1 = 3;
numero2 = 33;
// Definimos una función con dos argumentos
function sumar(num1,num2) {
	console.log("El resultado es: " num1 + num2);
}
// llamar a la función con los dos números.
sumar (numero1, numero2);
sumar (12, numero1);
</script>
```
+++
## Función (2) - Variable local
```
<script>
numero1 = 3;
numero2 = 33;
// Definimos una función con dos argumentos
function sumar(num1,num2) {
	**sumaTotal** = num1 + num2;
}
// llamar a la función con los dos números.
sumar (numero1, numero2);
console.log("El resultado es: " sumaTotal);
</script>
```
+++
## Función (3) - Variable global
```
<script>
numero1 = 3;
numero2 = 33;
// Definimos una función con dos argumentos
function sumar(num1,num2) {
	**var sumaTotal** = num1 + num2;
	return sumaTotal;
}
// llamar a la función con los dos números.
resultado = sumar (45, numero2);
console.log("El resultado es: " resultado);
</script>
```
+++
## Función (4) - Valores por defecto (1)
```
<script>
iva = 1.21;

function sumar_iva(precio,iva) {
	var precioFinal = precio * iva;
	return precioFinal;
}
precio = sumar_iva(45, iva);
alert("El precio es: " + precio);
</script>
```

+++
## Función (5) - Prompt() (1)
```
<script>
tuNombre = prompt("Introduce tu nombre:");
Console.log("Tu nombre es: " + tuNombre);
</script>
```
+++
## Función (5) - Prompt() (2)
```
<script>
function nombreCompleto(){
	var nombre= prompt("Introduce tu nombre:");
	var apellidos= prompt("Introduce tus apellidos:");
	
	var nombreYapellidos = nombre + " " + apellidos;
	return nombreYapellidos;
}
nombre1 = nombreCompleto(); 
alert(nombre1);
nombre2 = nombreCompleto(); 
alert(nombre2);
nombre3 = nombreCompleto(); 
alert(nombre3);
...
</script>
```
---

# OBJETO
# STRING 
+++
## Cadenas de Texto (Strings)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "       texto con espacios.       ";
console.log(nombre);
console.log(apellido);
console.log(texto);
</script>
```
+++
## Función “recortar” de String (1)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "       texto con espacios.       ";
console.log(nombre);
console.log(apellido);
console.log(texto);
// .trim() quita los espacios de una cadena de texto.
textosinespacios = texto.trim();
console.log(textosinespacios);
</script>
```
+++
## Función “recortar” de String (2)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "       texto con espacios.       ";
console.log(nombre);
console.log(apellido);
console.log(texto);
textosinespacios = texto.trimLeft();
textosinespacios = texto.trimRight();
console.log(textosinespacios);
</script>
```
+++
## Función “mayúsculas/minúsculas” de String
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto CON espacios.";
console.log(texto);
otrotexto = texto.toUpperCase();
console.log(otrotexto);
otrotexto = texto.toLowerCase();
console.log(otrotexto);
</script>
```
+++
## Función “trocear” de String
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "algo CON espacios.";
console.log(texto);
otrotexto = texto.slice(0,4);
console.log(otrotexto);
// Devolvería -> algo
</script>
```
+++
## Función “repetir” de String
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "algo CON espacios.";
console.log(texto);
otrotexto = texto.repeat(2);
console.log(otrotexto);
// Devolvería -> algo CON espaciosalgo CON espacios
</script>
```
+++
## Funciones Condicionales (1)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = texto.search("con");
console.log(res);
// Devolvería 6 -> el número del carácter donde empieza la palabra a buscar
// Devolvería -1 si no encuentra el texto
</script>
```
+++
## Funciones Condicionales (2)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = nombre.startsWith("D");
console.log(res);
// Devolvería 'true'.
// Devolvería 'false' si no empieza por la letra(s).
</script>
```
+++
## Funciones Condicionales (3)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = nombre.endsWith("i");
console.log(res);
// Devolvería 'true'.
// Devolvería 'false' si no acaba por la letra(s) 'i'.
</script>
```
+++
## Funciones Especiales (1)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = texto.split(" ");
console.log(res);
// Devolvería -> Array [ "texto", "con", "espacios]
</script>
```
+++
## Funciones Especiales (2)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = nombre.length;
console.log(res);
// Devolvería 4 -> El número de caracteres de la variable nombre
</script>
```
+++
## Funciones Especiales (3)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = texto.charAt(2);
console.log(res);
// Devolvería x -> El carácter en la posición 0, 1, 2.
</script>
```
+++
## Funciones Especiales (4)
```
<script>
nombre = "Dani"; 
apellido = String("Pastor");
texto = "texto con espacios.";
console.log(texto);

res = nombre.concat(" ",apellido);
console.log(res);
// Devolvería Dani Pastor
</script>
```
+++
+++
+++
+++
+++
