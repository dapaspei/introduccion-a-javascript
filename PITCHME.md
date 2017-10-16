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
<script type=“text/javascript”>
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
# Variable
### Es un elemento que contiene un valor. 
### Y ese valor puede variar.
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
### Cadenas de caracteres “Strings” (“Dani”)
### Números enteros “integer” (10)
### Números con decimales “float” (1.0)
### Valores lógicos “bolean” (true/false)
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
### Funciones mínimas para crear otras funciones
+++
### IF (1)
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
### IF (2)
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
### IF (3)
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
### IF (4)
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
### IF (5)
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
### SWITCH
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
### FOR
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
## Variable local
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
## Variable global
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
## Valores por defecto
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
## Prompt() (1)
```
<script>
	tuNombre = prompt("Introduce tu nombre:");
	Console.log("Tu nombre es: " + tuNombre);
</script>
```
+++
## Prompt() (2)
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
## “Recortar” (1)
### Función de String
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
## “Recortar” (2)
### Función de String
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
## “Mayúsculas” y “Minúsculas” 
### Función de String
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
## “Trocear” 
### Función de String
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
## “Repetir” 
### Función de String
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
## Condicionales (1)
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
## Condicionales (2)
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
## Condicionales (3)
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
	
	res = nombre.concat(" "+apellido);
	console.log(res);
	// Devolvería Dani Pastor
</script>
```
---
# ARRAYS
### Es un conjunto de elementos guardados en una variable
+++
```
<script>
	// Forma 1
	nombres_1 = new Array();
	// Inicializa un objeto.
	console.log(nombres_1);
	// Devuelve un array vacío.
	
	// Forma 2
	nombres_2 = Array();
	// Inicializa un objeto.
	console.log(nombres_2);
	// Devuelve un array vacío.
</script>
```
+++
```
<script>
	// Forma 3 y la recomendable!
	nombres_3 = [];
	// Inicializa un objeto.
	console.log(nombres_3);
	// Devuelve un array vacío.
</script>
```
+++
```
<script>
	nombres_1 = new Array();
	nombres_2 = Array();
	nombres_3 = [];
	
	nombres = [ “Dani”, “John”, “Herald”];
	console.log(nombres);
	// Devuelve un array con los tres nombres
	console.log(nombres.length);
	// Devuelve 3. El número de elementos que tiene el array
</script>
```
+++
```
<script>
	nombres_1 = new Array();
	nombres_2 = Array();
	nombres_3 = [];
	
	nombres = [ “Dani”, “John”, “Herald”];
	console.log(nombres);
	// Devuelve un array con los tres nombres
	console.log(nombres.length);
	// Devuelve 3. El número de elementos que tiene el array
</script>
```
+++
```
<script>
	edades = [8, 12, 34, 23, 87];
	console.log(edades);
	// Devuelve un array con 5 elementos
	console.log(edades.length);
	// Devuelve 5. El número de elementos que tiene el array
</script>
```
+++
### Crear elementos. ¡Ojo!
```
<script>
	edades = [8];
	// Crea un array con un elemento, el 8.
	edades = Array(8);
	// Crea un array con 8 elementos!!
	console.log(edades);        // Devuelve un array vacío.
	console.log(edades.length); // Devuelve 8
</script>
```
+++
### Añadir elementos
```
<script>
	nombres = [];
	// Añadir elementos.
	nombres.push("Dani");
	console.log(nombres);
	// Devuelve "Dani"
	console.log(nombres.length);
	// Devuelve 1
</script>
```
+++
### Acceder a un elemento
```
<script>
	nombres = ["Dani"];
	// Añadir elementos.
	nombres.push("John");
	nombres.push("Maria");
	nombres.push("Eldelbar");
	console.log(nombres);
	// Devuelve "Dani", "John", "Maria", "Eldelbar"
	console.log(nombres[0]);
	// Devuelve "Dani"
</script>
```
+++
### Borrar un elemento
```
<script>
	nombres = ["Dani"];
	// Añadir elementos.
	nombres.push("John");
	nombres.push("Maria");
	delete nombres[1];
	// Borra "John", dejando el "hueco" en el array.
	console.log(nombres);
	console.log(nombres.length);
	// Devuelve 3
</script>
```
+++
### Actualizar elementos
```
<script>
	nombres = ["Dani"];
	// Añadir elementos.
	nombres.push("John");
	nombres.push("Maria");
	nombres[1] = "Peter";
	// Cambia "John" por "Peter"
	console.log(nombres);
	// Devuelve "Dani", "Peter", "Maria"
</script>
```
---

# BUCLES
+++
### FOR
```
<script>
	for (var contador = 0; // Se ejecuta únicamente 1 vez
			 contador < 10;    // Es una comparación
			 contador++        // contador = contador + 1
												 // Incrementa la variable una unidad
			 ) {
			 // El código entre paréntesis se ejecuta si la comparación
			 // da como resultado -> 'true'
			 console.log("El contador vale: " + contador);
			 // Aparece desde 0 --- 9
			 // No aparece 10, porque 10 no es < 10.
	}
</script>
```
+++
### WHILE (1)
```
<script>
  // Similar al FOR. Se ejecuta de forma indefinida
  // hasta que se indica lo contrario.
  var nombre = "Dani";
  var contador = 0;
	while (nombre == "Dani") {
		console.log("El contador vale: " + contador);
		contador++;
	}	
	// OJO!!! Esto crea un bucle infinito que bloqueará el navegador.
</script>
```
+++
### WHILE (2)
```
<script>
  var admin = true;  // El usuario es administrador.
  // while (admin == true) {
	while (admin) { 
		console.log("Soy el administrador.");
		admin = false;
		// Dejará de ejecutarse el bucle, porque admin valdrá 'false'
	}	
</script>
```
+++
### DO WHILE
```
<script>
  var admin = true;  // El usuario es administrador.
  
  // El bucle se ejecutará al menos 1 vez.
	do {
		console.log("Soy el administrador.");
		admin = false;
		// Dejará de ejecutarse el bucle, porque admin valdrá 'false'
	} while (admin);
</script>
```
+++
### Recorrer Arrays (1)
```
<script>
  var nombres = ["Dani", "Juan", "Petra", "Luisa", "Juan"];
  // dato es el **valor** de cada elemento del array.
  // aunque sólo tenga una parte el for, se ejecutará hasta que 
  // haya nombres en el array.
  
  for (var dato of nombres) {
	  // dato OF nombres -> devuelve el valor
	  console.log(dato);
  }
  // Devuelve -> Dani, Juan, Petra, Luisa, Juan.
  </script>
```
+++
### Recorrer Arrays (2)
```
<script>
  var nombres = ["Dani", "Juan", "Petra", "Luisa", "Juan"];
  // dato es el **índice** de cada elemento del array.
  // aunque sólo tenga una parte el for, se ejecutará hasta que 
  // haya nombres en el array.
  
  for (var dato in nombres) {
	  // dato IN nombres -> devuelve el índice
	  console.log(dato);
  }
  // Devuelve -> 0, 1, 2, 3, 4
  </script>
```
+++
### Recorrer Arrays (3)
```
<script>
  var nombres = ["Dani", "Juan", "Petra", "Luisa", "Juan"];
  // dato es el **índice** de cada elemento del array.
  // aunque sólo tenga una parte el for, se ejecutará hasta que 
  // haya nombres en el array.
  
  for (var contador=0; contador < nombres.length; contador++) {
	  // nombres.length es el número de elementos del array
	  console.log(nombres[contador]);
	  // nombres[contador] se corresponderá con cada nombre.
  }
  // Devuelve -> Dani, Juan, Petra, Luisa, Juan.
  </script>
```
---
# FUNCIONES NATIVAS
+++
### encodeURI()
```
<script>
	// codifica el texto para convertirlo en una URL válida
	tmp = encodeURI("http://google.com/search?q=algo que buscar"); 
	console.log (tmp); 
	// Devolverá: http://google.com/search?q=algo%20que%20buscar
</script>
```
### Es importante para generar nuestras propias URLs en Javascript.
+++
### decodeURI()
```
<script>
	// DEcodifica la URL válida para convertirla en texto
	tmp = decodeURI("http://google.com/search?q=algo%20que%20buscar"); 
	console.log (tmp); 
	// Devolverá: http://google.com/search?q=algo que buscar
	// Ahora la URL sólo es válida hasta "algo".
</script>
```
+++
### alert()
```
<script>
	// Tiene un solo argumento
	// Muestra un mensaje en una nueva ventana.
	// Tiene un único botón -> Aceptar.
	alert("Hola mundo!");
	// Esta función no devuelve nada
	tmp = alert("Adios!");
	console.log(tmp);
	// Devolverá: undefined
</script>
```
+++
### prompt()
```
<script>
	// Tiene un solo argumento
	// Podemos introducir un texto.
	// Tiene dos botones -> Aceptar / Cancelar.
	tmp = prompt("Nombre: ");
	console.log(tmp);
	// Esta función devuelve el nombre introducido
	// ---
	// Pero si le damos al botón "Cancelar", devolverá:
	// NULL
	// 'null' es un valor especial.
</script>
```
+++
### confirm()
```
<script>
	// Tiene un solo argumento
	// Muestra un texto.
	// Tiene dos botones -> Aceptar / Cancelar.
	tmp = confirm("¿Deseas salir de la página?");
	console.log(tmp);
	// Esta función devuelve 
	// 'true' si le damos a aceptar
	// 'false' si le damos a cancelar.
	if (confirm("¿Deseas salir de la página?")) {
		alert("Es una lástima, pero ... Adiós!");
	}
</script>
```
+++
### JSON
#### JavaScript Object Notation
> Es un formato de texto para intercambiar datos entre distintos lenguajes de programación.
+++
### JSON
```
<script>
	nombres = ["Dani", "Jaimito", "Juanito", "Jorgito", "John"];
	console.log(nombres);
	tmp = JSON.stringify(nombres);
	console.log(tmp);
	// Devuelve un String con los nombres también, pero en un único string.
</script>
```
+++
### setTimeout() (1)
```
<script>
	// Recibe dos argumentos
	// Argumento 1: la función a ejecutar. 
	// Argumento 2: cuándo se ejecutará. En milisegundos!!
	function prueba() {
		console.log("Me estoy ejecutando!");
	}
	setTimeout(prueba, 3000);
	// Tardará 3 segundos en aparecer el mensaje en la consola.
</script>
```
+++
### setTimeout() (2)
```
<script>
	// Recibe dos argumentos
	// Argumento 1: la función a ejecutar. 
	// Argumento 2: cuándo se ejecutará. En milisegundos!!
	function prueba() {
		console.log("Me estoy ejecutando!");
	}
	setTimeout(prueba, 3000);
	// Tardará 3 segundos en aparecer el mensaje en la consola.
  console.log("El resultado de la suma es: ",  2 + 3);
  // ¿Se mostrará el resultado de la suma después del mensaje de 3 segundos??
  // NO! Se ejecutará primero el resultado de la suma y luego el mensaje
</script>
```
+++
### setInterval
#### Ejecutar un código de forma ilimitada durante X segundos
```
<script>
	// Recibe dos argumentos
	// Argumento 1: la función a ejecutar. 
	// Argumento 2: el intervalo de tiempo en milisegundos!!
	function prueba() {
		console.log("Me estoy ejecutando!");
	}
	setInterval(prueba, 3000);
	// Cada 3 segundos aparecerá el mensaje en la consola.
	// Esto NO bloqueará el navegador!!
	// Se puede utilizar para comprobar las Cookies.
  </script>
```
+++
### Funciones anónimas
```
<script>
	// Definimos una función dentro de otra función.
	setInterval(function(){
		console.log("Me estoy ejecutando!");
	}, 3000);
	// Cada 3 segundos aparecerá el mensaje en la consola.
  </script>
```
+++
### Typeof
```
<script>
	// Definimos una función dentro de otra función.
	setInterval(function(){
	  // Únicamente le damos el valor 1 al contador si no está definido
	  // Sino, contador siempre valdría 1.
		if(typeof contador == "undefined"){
			contador = 1;
		}
		console.log(contador + " - se ejecuta correctamente!");
		contador++;
	}, 3000);
	// Cada 3 segundos aparecerá el mensaje en la consola.
  </script>
```
---
# OBJETOS
+++
### Tratar con OBJETOS consiste en parametrizar un objeto de la vida real y dotarles de funcionalidades.
+++
```
<script>
	// Objeto "móvil".
	movil = {
		// Parámetros
		marca: "iPhone",
		modelo:  "X",
		precio: 1.200,
		procesadores: 2,
		ram:2,
	};
	
	console.log("La marca es: " + movil.marca);
  </script>
```
+++
```
<script>
	// Objeto "móvil".
	movil = {
		// Parámetros
		marca: "iPhone",
		modelo:  "X",
		precio: 1.200,
		procesadores: 2,
		ram:2,
		// Funcionalidades
		llamar: function(nombre) {
			console.log("Estoy llamando a " + nombre +" con el "+this.marca); 
			// This es el objeto que llama a la función
		}
	};
	movil.llamar("Dani");
	// Salida: Estoy llamando a Dani con el iPhone
	</script>
```
+++
```
<script>
	// Objeto "persona".
	usuario = {
		// Parámetros
		nombre: "Dani", apellido: "Pastor", 	edad: 33,	permisos: true,
		hijos: ["Alejandro", "Javier"],
		// Funcionalidades
		nombre_completo: function() {
			alert(this.nombre + " " + this.apellido);
		}
		mayor_edad: function() {
			if (this.edad >= 18) {
				console.log("Eres mayor de edad!");
			} else {
				console.log("Eres menor de edad!");
			}
		}
	};
	usuario.nombre_completo();
	// Devuelve: Dani Pastor
	usuario.mayor_edad();
	// Devuelve: Eres mayor de edad!
	</script>
```
---
# HTML y Javascript
+++
### Acceso por ‘id’
```
<div>
	<div id="lorem" class=“mitexto”>
		Lorem ipsum ad his scripts blandit ....
	</div>
	<form action=“” method=“” name=“miformulario”>
		<p>Nombre:</p> <input type=“text” name=“nombre”>
		<p>Email:</p> 	<input type=“text” name=“email”>
		<p>Contraseña:</p> <input type=“text” name=“password”>
	</form>
</div>
// Se sitúa debajo para que el id="lorem" exista.
<script>
	// Coge el elemento que tenga el Id -> Lorem
	console.log(document.getElementById("lorem").innerHTML = "Nuevo texto....");
	// Cambia el texto por "Nuevo Texto"
</script>
```
+++
### Window.onload
```
<script>
	// Obliga a que se carga el html antes de ejecutar Javascript
	window.onload = function() {
		var name = prompt("Nombre:");
		var apellido = prompt("Apellidos");
		document.getElementById("lorem").innerHTML = name +" "+apellido;
	}	
</script>
</head>
<body>
	<div>
		<div id="lorem" class=“mitexto”>
			Lorem ipsum ad his scripts blandit ....
		</div>
		<form action=“” method=“” name=“miformulario”>
			<p>Nombre:</p> <input type=“text” name=“nombre”>
			<p>Email:</p> 	<input type=“text” name=“email”>
			<p>Contraseña:</p> <input type=“text” name=“password”>
		</form>
	</div>
```
+++
### Acceso por ‘clase’
```
<script>
	window.onload = function() {
		var name = prompt("Nombre:");
		var apellido = prompt("Apellidos");
		// Acceso por el nombre de la clase.
		document.getElementsByClassName("mitexto")[0].innerHTML = name +" "+apellido;
	}	
</script>
</head>
<body>
	<div>
		<div id="lorem" class=“mitexto”>
			Lorem ipsum ad his scripts blandit ....
		</div>
		<form action=“” method=“” name=“miformulario”>
			<p>Nombre:</p> <input type=“text” name=“nombre”>
			<p>Email:</p> 	<input type=“text” name=“email”>
			<p>Contraseña:</p> <input type=“text” name=“password”>
		</form>
	</div>
```
+++
### Acceso por ‘nombres’
```
<script>
	window.onload = function() {
		var name = prompt("Nombre:");
		var email = prompt("Email");
		var password = prompt("Password");
		document.getElementsByName("nombre")[0].value = name;
		document.getElementsByName("email")[0].value = email;
		document.getElementsByName("password")[0].value = password;
	}	
</script>
</head>
<body>
	<div>
		<div id="lorem" class=“mitexto”>
			Lorem ipsum ad his scripts blandit ....
		</div>
		<form action=“” method=“” name=“miformulario”>
			<p>Nombre:</p> <input type=“text” name=“nombre”>
			<p>Email:</p> 	<input type=“text” name=“email”>
			<p>Contraseña:</p> <input type=“text” name=“password”>
		</form>
	</div>
```
+++
### Formularios
```
<script>
	window.onload = function() {
		var name = prompt("Nombre:");
		var email = prompt("Email");
		var password = prompt("Password");
		window.miformulario.nombre.value = name;
		window.miformulario.email.value = email;
		window.miformulario.password.value = password;
	}	
</script>
</head>
<body>
	<div>
		<div id="lorem" class="mitexto">
			Lorem ipsum ad his scripts blandit ....
		</div>
		<form action=“” method=“” name="miformulario">
			<p>Nombre:</p> <input type=“text” name="nombre">
			<p>Email:</p> 	<input type=“text” name="email">
			<p>Contraseña:</p> <input type=“text” name="password">
		</form>
	</div>
```
