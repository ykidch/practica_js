# Resumen

- **3 maneras de insertar CSS:**
```html
	<tag style="attribute:value; attribute:value; ...">
```
  
```html
	<style>
		h1 {color:red;...}
		.class {...}
		#id {...}
	</style>
```
  
```html
	<link href="path/to/file" type="text/css" rel="stylesheet">
```

- **Maneras de insertar JS**
```html
	<script>
		...
		código JS
		...
	</script>
```
  
```html
	<script src="myscript.js"></script> 
	<!--(se comporta igual que si copias y pegas el código directo en el html)-->
```



## JavaScript
  
- **Documentación**  

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference)  

e.g. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
(te dice desde qué versiones de buscadores es compatible)

- **Generalidades**
```js
// éste es un comentario
```
```js
/* así comentas
   muchas líneas */ 
```
  
```js
var foo = valor;	// declara una variable
foo = valor2;		// cambiar el valor de una variable (ya declarada)
```
  
```js
console.log(foo);	// como "print" o "echo"
```

- **Tipos de datos importantes:**
	- número: 1,2,3
	- string: 'abc'
	- array: [1,2,3,'a','b','c']   -  array[i] (indexar desde 0)
	- objeto: {key1:value1, key2:value2, ...}  - objeto.key

- **if, for, while, switch**
```js
if (condición) {
	acción
	}
else if (condición) {
	acción
	}
else (condición) {
	acción 
	};
```
  
```js
switch (variable) {
	case "a":
		...
		break;
	case "b":
		...
		break;
	...
	default:
		...
		break;
	}
```
  
```js
for (var i=min; i<=max; i++) {
	acción
	};
```
  
```js
while (condición) {
	acción
	};
```
  
- Definir funciones

```js
function miFuncion(args) {
	...
	return valor;
	}	
```

## El DOM
  
- JS interactúa con HTML con el "DOM"
  
- **Extraer elementos**
  
```js
document - todo el contenido de la página
document.getElementById('id')
document.getElementsByClassName('classname') 
document.getElementsByTagName('tagname') 
document.querySelector('#id'/'.classname'/'tagname')
	document.querySelector('tag.class#id')
```

- **Extraer/modificar contenido de elementos**
  
```js
Element.innerHTML	//regresa el HTML dentro del elemento (puedes cambiarlo)
Element.textContent	//regresa el contenido sin contar los HTML tags (puedes cambiarlo)

Element.style.attribute = nuevo_valor	// modifica el CSS
Element.setAttribute('attribute','value')
```

- **Introducir elementos**

```js
document.createElement('tag')	//crea <tag></tag> (pero no lo mete en el DOM)

// Para meter elementos en el DOM:
Element.appendChild(otherElement)	//mete otherElement como un hijo de Element, justo antes de </Element>
Element.insertAdjacentElement(where,otherElement)	//inserta otherElement en:
/*
	where = 'beforebegin' - hermano antes de Element
		'afterbegin' - justo después de <Element>
		'beforeend' - justo antes de </Element>
		'afterend' - hermano después de Element 
*/
```

- **Quitar elementos**
```js
Element.removeChild(childElement)
Element.remove()
```

- **Eventos**
```js
document.addEventListener(evento, funcion)
Element.addEventListener(evento, funcion)
```

- **Tiempo**
```js
setTimeout(funcion,ms)
	setTimeout(function(){ alert("Hello"); }, 3000);
	setTimeout(miFunction, 3000)

setInterval(function,ms)

clearTimeout()
	var myVar = setTimeout(...)
	clearTimeout(myVar)

clearInterval()

var d = newDate();
var n = d.getTime();
```
