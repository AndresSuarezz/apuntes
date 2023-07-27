# Sobre useEffect

Este siempre es un callback, que se ejecuta cuando un state cambia o cuando el componente esta listo.

## Usos de useEffect

Al ejecutarse automaticamente cuando el componente esta listo, es un excelente lugar para colocar código para consultar una API o LocalStorage.

Debido a que le podemos pasar una dependencia y estar escuchando por los cambios que sudedan en una variable, puede actualizar el componente cuando ese cambio suceda.

## Sintaxis

```jsx
import { useEffect } from "react";

useEffect(() => {
  console.log("El componente esta listo");
}, []);
```
