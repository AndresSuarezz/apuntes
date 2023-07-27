# Como instalar TailwindCss

Para instalar tailwind debes ejecutar este comando en la terminal

```
npm i -D tailwindcss
```

Para el proyecto de veteriaria

```
npm i -D tailwindcss postcss autoprefixer
```

Requerimos un archivo de configuracion de Tailwind y de Postcss

```
npx tailwind init -p
```

Agregar esta configuracion a nuestro `index.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Por ultimo modificamos el fichero `tailwind.config.js` de la siguiente manera

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["index.html", "./src/**/*.jsx"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

En el `content` van aquellos archivos a los que le queremos aplicar tailwind.

Tailwind CSS resetea todos los componentes
