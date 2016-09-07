# leccion-20-1

Modificar el siguiente script usando closures para que se ejecute sin problemas.

```javascript
var num2 = 0;

function suma(num1) {
	return function() {
		return num1 + num2;
	}
} 

var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado

var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.
```

Para un Closure necesitamos dos funciones (padre-hijo), las cuales tenemos, pero la funcion hijo no tiene un parametro el cual necesita asi que agregandolo a la funcion anónima esta funcion sera capaz de coger el resuktado que pide el console.log.

```javascript
function suma(num1) {
	return function(num2) { //parametro agregado
		return num1 + num2;
	}
} 

var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado

var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.
```

