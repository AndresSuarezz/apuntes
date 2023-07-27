# Que son los Hooks en React?

React cuenta con una API muy sencilla que te permite crear todo ripo de aplicaciones por medio de algo llamado Hooks.

Los Hooks están disponibles desde la version 16.8, previo a ello se tenían que crear classes para crear y modificar el state, con los Hooks no es necesario.

Se dividen en basicos y en adicionales

| Basicos    | Adicionales         |
| ---------- | ------------------- |
| useState   | useReducer          |
| useEffect  | useCallback         |
| useContext | useMemo             |
|            | useRef              |
|            | useImperativeHandle |
|            | useLayoutEffect     |
|            | useDebugValue       |

Tambien es posible hacer los propios Hooks, de esta forma se podrá separar el codigo en funciones reutilizables y scar todo el beneficio de lo que React ofrece.

Como puedo usar estos Hooks

```js
import { useState, useEffect } from "react"; //Importamos
const yuca = () => {
  return <div>yuca</div>;
};

export default yuca;
```

## Que es el state?

El state o estado es básicamente eso; cuál es el estado de nuestra aplicación.

El estado es una variable con información relevante en nuestra aplicación de React, algunas veces el state pertenece a un componenete en especifico o algunas veces deseas compartirlo a lo largo de diferentes componenetes.
Para usar el State es de esta manera

```js
import { useState } from "react";

const [cliente, setCliente] = useState({});
```
El `cliente` es la variable, el `setCliente` se le conoce como el modificador de la variable `cliente`, por ultimo el `useState({})` que es el que indica el valor inicial, en el ejemplo se inicia con un objeto vacio.

## React reacciona `En base al State`
Cadad que el state cambia, la aplicacion de React va a renderizar y actualizarse con esos cambios.

Para modificar el state, se utiliza la función que extraemos cuando declaramos el state en nuestro componente, es decir, el `setCliente`:

## Reglas de los Hooks
Los Hooks se colocan en la parte superior de tus componenetes de React.

No se debe colocar dentro de condicionales, tampoco después de un return.

## Eventos en React
La forma en que React maneja los eventos es muy similar a como hace JavaScript de forma nativa con algunos cambios.

Los eventos son camelCase, es decir en lugar de onchange se utiliza onChange, en lugar en onclick se utiliza onClick.

Tambien a diferencia de JS y HTML, donde se coloca el nombre de la funcion en un string en React (JSX) se utiliza la función.

### Sintaxis
En HTML:
~~~HTMl
<button onclick="descargarPedidos()">Descargar Pedidos</button> 
~~~
En JSX
~~~HTML
<button onClick={descargarPedidos()}>Descargar Pedidos</button>
~~~

Otro ejemplo pero con un formulario:
En HTML
~~~HTML
<form onsubmit="agregarCliente()"; return false>
    <button type="submit">Submit</button>
</form>
~~~
En JSX
~~~HTML
<form onsubmit={handleSubmit}>
    <button type="submit">Añadir Cliente</button>
</form>
~~~