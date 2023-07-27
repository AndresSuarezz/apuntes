# Que es JSX

---

JSX(JavaScript Syntax Extension)

Es una extensión del lenguaje desarrollada por Facebook para React.

Parece JS pero muestra código de HTML, y básicamente es un lenguaje de Template que muestra el HTML pero tiene todas las funciones de JavaScript.

Una vez compilado son archivos JS con funciones y objetos.

## Reglas en JSX

A diferencia de HTML, que no es estricto, en JSX si un elemento HTML tiene una etiqueta de apertura, deberás tener también la de cierre.

Las etiquetas de solo apertura como `<link>` `<img>` o `<input>` deberán finalizar con `/>`

Cada componente debe tener un return.
En este return debe haber máximo un solo elemento en el nivel máximo.

## Cosas que se pueden hacer para antes del `return()`

Se pueden crear funciones, validaciones, etc. Por ejemplo:

```jsx
function App() {
  const sumar = () => {
    const numero = 5;
    if (numero > 5) {
      console.log("Si es mayor");
    } else {
      console.log("No es mayor");
    }
    console.log(2 + 2);
  };
  sumar();

  return (
    <>
      {1 + 1}// Si queremos ejecutar js en el render
      <h1>Hola Mundo</h1>
    </>
  );
}
```

De esta manera podemos usar ternarios en el codigo, para evaluar y mostrar una informacion:

```jsx
function App() {
  const edad = 18;

  return (
    <>
      {edad >= 18 ? "Eres mayor" : "No eres mayor"}
      <h1>Hola Mundo</h1>
    </>
  );
}
```

Tambien podemos mostrar variables que hayamos creado

```jsx
function App() {
  const edad = 18;

  return (
    <>
      <h1>{edad}</h1>
    </>
  );
}
```
