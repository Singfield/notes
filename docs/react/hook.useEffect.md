# useEffect

UseEffect permet d'executer du code après n'importe quel rendu ou
re-rendu.

Permet de "connecter les elements exetieurs avec le reste de l'application.

```JS 
React.useEffect(()=>{
    window.localStorage.setItem(key, state)
  },[key, state])
```

UseEffect accepte en premier lieu une callBack qui contiendra le code a executer.

En second lieu un tableau de dépendances qui permettront au useEffect de s'executer uniquement si une des dépendances est modifiée.
Ainsi cela ne dépendra plus de l'arbre des composants.

## useState

représente le state du composant.
```JS
  const [state, setState] = React.useState(
    ()=> window.localStorage.getItem(key) ?? defaultValue
  )
```

## lasy state initialisation

parfois nous ne voulions pas que react met a jour un state directement. On aimerait qu'il prennent un peu de temps avant d'update le state.

Pour ça on a juste a passer une callback en guise de valeur par defaut dans la hook useState.

```JS
function useLocalStorage (key, defaultValue =''){
  const [state, setState] = React.useState(
    ()=> window.localStorage.getItem(key) ?? defaultValue
  )
```



