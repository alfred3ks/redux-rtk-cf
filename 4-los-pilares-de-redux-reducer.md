# Los pilares de Redux: Los Reducers:

Reducer es la antesala que va a actualizar al store. Es un paso antes de actualizar la store.

Son funciones (puras) que regresan una pieza (key) del estado global de la store dependiendo de la accion (type) que se le ha enviado.

Asi luce un reducer:

```javascript
// Tenemos el action:
const ADD_TODO = 'ADD_TODO';

function addTodo(text) {
  return {
    type: ADD_TODO,
    text,
  };
}

// Tenemos el reducer:
const todoApp = (state = initialState, action) => {
  switch (action.type) {
    case ADD_TODO:
      return {
        ...state,
        text: action.text,
      };
    default:
      return state;
  }
};
```

Vemos que es una funcion que recibe 2 parametros, uno es el estado que esta inicializado, bien sea a un objeto vacio {}, una constante, esto es para que el store no se declare undefined al inicio. Como segundo parametro recibe el action.

Con el return lo que hacemos es actualizar el store. Estas funciones dentro del flujo de redux es que podemos actualizar la store.

Vemos con el ejemplo:

```javascript
// Tenemos el action:
const FETCH_POKEMON_BY_NAME = 'FETCH_POKEMON_BY_NAME';

const fetchPokemonsByName = (name) => ({
  type: FETCH_POKEMON_BY_NAME,
  name,
});

// Aqui tenemos un reducer:
const pokemonsReducer = (state = {}, action) => {
  switch (action.type) {
    case FETCH_POKEMON_BY_NAME:
      return {
        ...state,
        pokemon: action.name,
      };
    default:
      return state;
  }
};
```
