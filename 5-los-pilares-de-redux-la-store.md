# Los pilares de Redux: La store:

Es donde se va a concentrar toda la información venga de donde sea.

La stores es un mega objeto, {} que contiene todos los keys (reducers) con la información global que puede ser consumida por tus componentes. Como luce esta store:

```javascript
{
  pokemons:{},
  user:{},
  locationInfo: {}
}
```

```javascript
{
  pokemons:{
    data:[{...}]
  },
  user:{
    id:'somefakeid',
    name:'John Doe',
    age:22
  },
  userPreferences: {}
}
```

Como vemos este objeto tiene kew, esos keys son los reducer.
