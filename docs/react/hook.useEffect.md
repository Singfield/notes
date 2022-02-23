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



