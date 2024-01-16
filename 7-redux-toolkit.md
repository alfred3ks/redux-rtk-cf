## Redux toolkit:

Redux, es la herramienta, el manejador de estado. Es el flujo, los actions, reducers, store. Pero luego llego Redux Toolkit, es como una envoltura de Redux para hacerlo mas simple, para hacer la configuración de una manera mas fácil.

Configurar redux es algo complicado, para eso usaremos redux toolkit. Cuando instalamos redux hay que instalar un monton de cosas que con redux toolkit ya viene instalados.

Redux toolkit fue creado por los creadores de Redux.

# Pasos para configurar Redux Toolkit:

- Importar y crear un reducer principal.
- Configurar un middleware para el trabajo asincrono.
- Configurar la extension de Redux DevTools.

# Instalación y configuración de redux toolkit en el proyecto recetas:

Podemos ver la documentacion de redux toolkit:

https://redux-toolkit.js.org/

https://redux-toolkit.js.org/tutorials/quick-start

Como es para un proyecto existente tenemos que ejecutar:

```bash
npm install @reduxjs/toolkit react-redux
```

Vamos al proyecto de recetas y hacemos la instalación.

Ahora siguiendo la documentación nos dice que creemos un Redux Store, en la carpeta src del proyecto nos creamos una carpeta que se llame redux. Dentro de esta carpeta creamos tambien una llamada actions, otra llamada store, y otro que se llame reducers. Dentro del store creamos nuestro index.js

Ahora dentro de este archivo es donde vamos a colocar la configuración que nos recomiendan en la documentacion:

## store/index.js:

```javascript
import { configureStore } from '@reduxjs/toolkit';

// Configuramos la store:
export default configureStore({
  reducer: {},
});
```

Ahora lo que vamos es a conectar la store. Tenemos que colocar un provider que englobe toda la aplicación.

Este provider lo vamos a colocar en main.jsx:

# main.jsx:

```javascript
// Importamos el proveedor:
import Provider from 'react-redux';

// Importamos la store:
import store from './redux/store';

// Envolvemos el componente app por medio del provider y le pasamos una propiedad store que es un objeto:
<Provider store={store}>
  <BrowserRouter>
    <App />
  </BrowserRouter>
</Provider>;
```

Ya tenemos conectada nuestra aplicación con la store. Ya tenemos el objeto vacio lista para recibir las acciones.
