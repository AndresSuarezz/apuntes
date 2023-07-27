# Que son los Props?

## Variables o funciones de un componente a otro

El state o funciones que crees en tus componenets, solo estarán disponibles en ese componente.

Una forma de evitar duplicar código y reutilizar esas variables, state o estado y funciones en otros componentes es por medio de Props o Propiedades.

Los props se pasan del Padre al Hijo

## Sintaxis

```html
<Header nombreProp="{" datos o funciones } />
```
Ejemplo:
```html
<Header 
    clientes = { cliente } 
    admin = { false }
    setClientes = { setClientes }
    titulo = "Tienda virtual"
/>
```

Los props se pasan `desde el padre hacie el hijo`. Si tienes un state que se va pasar por diferentes componentes, lo mejor es colocarlo en el archivo principal.

Cada nivel de componentes deberá tomar y pasar el Prop hacia otros componentes, tecnologías como Redux o Context evitan tener que hacerlo de esta forma.

Para solucionar depronto algun problema con los props

```js
//Validacion de props 
  Formulario.propTypes = {
    pacientes,
    setPacientes
  }
```