# Los pilares de Redux: Los Actions:

Son funciones (puras) que regresan un objeto plano, caracterizandose por un unico tipo (type)

```javascript
{
  type: ADD_TODO,
  text: 'Build my first Redux app'
}
```

Aqui vemos como luce un action: Lo tenemos con una función normal y con una flecha, como vemos es una función que retorna un objeto con un tipo, ese tipo lo podemos ver como un ID de esa accion:

```javascript
const ADD_TODO = 'ADD_TODO';

function addTodo(text) {
  return {
    type: ADD_TODO,
    text,
  };
}

const addTodo = (text) => ({
  type: ADD_TODO,
  text,
});
```

Veamos otro ejemplo:

```javascript
const FETCH_POKEMON_BY_NAME = 'FETCH_POKEMON_BY_NAME';

const fetchPokemonsByName = (name) => ({
  type: FETCH_POKEMON_BY_NAME,
    name,
})

};

console.log(fetchPokemonsByName('pikachu'));

Vemos que nos retorna el objeto con un type:

{type: 'FETCH_POKEMON_BY_NAME', name: 'pikachu'}
```

Es de buenas prácticas el type colocarlo en una variable como vemos.
