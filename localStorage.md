# LocalStorage
En el localStorage no se pueden guardar arreglos, unicamente strings.

Como podemos usarlo? cuando estamos guardando, editando o elimiando queremos que esa informacion sea almancenada, entonces usamos localStorage para guardarlo en memoria, hacemos uso de `localStorage` y accedemos a su metodo `.setItem()`, dentro nos pedira una key y la informacion, ejemplo:

```jsx
localStorage.setItem(key, value)
```

En algunos casos el valor que queremos guardar puede ser un arreglo u otro tipo de dato, para eso usamos `JSON.stringify()` para convertir aquellos datos a un string

## Como puedo capturar la informacion que ya esta guardada?
Se pueden usar distintos useEffect uno para que cargue la informacion guardada, y luego otro que la cambie cuando esta informacion se edite, es decir, que se sincronize con el state.

```jsx
useEffect(() => {
    //Obtener informacion del LocalStorage
    const obtenerLocalStorage = () => {
      const pacientesLocalStorage = JSON.parse(localStorage.getItem('pacientes')) ?? [];
      setPacientes(pacientesLocalStorage);
    }
    obtenerLocalStorage();
  }, []);

  useEffect(()=>{
    //Guardar en el localStorage
    localStorage.setItem('pacientes', JSON.stringify(pacientes));
  },[pacientes]);
```
