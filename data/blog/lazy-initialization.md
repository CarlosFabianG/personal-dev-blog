---
title: useState lazy initialization en React
date: '2022-04-02'
tags: ['React', 'javascript', 'frontend']
draft: false
summary: Con esta técnica puedes optimizar el performance de tus aplicaciones React
---

Cuando nos adentramos al mundo de los hooks en React.js el primero que aprendemos es **`useState`**. Lo cual no es de extrañar ya que el manejo de estado es la parte crucial de un frontend basado en componentes. 

Aquí un ejemplo básico de su uso en un componente contador que responde al click de un botón:

```jsx
function Counter() {
  const [count, setCount] = React.useState(0)
  const increment = () => setCount(count + 1)
  return <button onClick={increment}>{count}</button>
}
```

En el ejemplo llamamos **`useState`** y por medio de ***array destructuring*** regresamos un array con el valor del estado y una función para actualizar el estado, también conocido como ***setter***. Cuando llamas el setter con el nuevo valor se dispara un re-render del componente por lo que se llama de nuevo **`useState`** para obtener el nuevo valor del estado y la función setter.

Esta es de las primeras cosas que aprendemos sobre el estado dentro del mundo de react.js. Sin embargo, hay una técnica menos conocida pero que nos puede traer una importante optimización en términos de performance en algunos casos específicos. 

```jsx
function Counter() {
  const [count, setCount] = React.useState(() => 0)
  const increment = () => setCount(count + 1)
  return <button onClick={increment}>{count}</button>
}
```

Como observamos, la diferencia es que en este segundo ejemplo pasamos una función que retorna el valor inicial de **`useState`** en lugar ****de solo el valor.  Los dos ejemplos funcionan igual pero hay algunas diferencias sutiles que son el objetivo de este post.

## Lazy initialization

Si colocáramos un ***`console.log`*** con el string `"hola mundo"` en nuestra función `counter`, este se imprimiría cada vez que damos click al botón. Esto es porque cada vez que la función `counter` es llamada en cada render se ejecuta todo el cuerpo de la función.

Lo anterior también significa que variables o parámetros, inicializados dentro de la función, son creados y evaluados en cada render. La mayoría de ocasiones esto no importa porque los motores de javascript optimizan estos casos:

```jsx
const initialState = 0
const [count, setCount] = React.useState(initialState)
```

En cambio, no sería lo mismo si el valor inicial de useState es computacionalmente demandante. 

Por ejemplo, un caso práctico podría ser si necesitamos pasar como el valor inicial de estado el ***local storage*** que es una operación IO costosa:

```jsx
const initialState = Number(window.localStorage.getItem('count'))
const [count, setCount] = React.useState(initialState)
```

El único momento en donde React necesita el valor inicial de useState es al inicio. Lo que signifca que solo lo necesita en el primer render. Pero puesto que el cuerpo de nuestra función counter corre en cada re-render de nuestro componente, nuestro código computacionalmente costoso se ejecuta en cada render incluso si no es necesario. 

En esos casos es cuando ***lazy initialization*** llega al rescate. Con esta técnica podemos colocar como valor inicial una función. 

```jsx
const getInitialState = () => Number(window.localStorage.getItem('count'))
const [count, setCount] = React.useState(getInitialState)
```

Lo anterior funciona porque incluso si lo que la función hace es costoso en términos computacionales, solo se paga el precio cuando llamas a la función en cuestión. Entonces, si pasas una función a `**useState**`, React solo llamará la función cuando el valor inicial sea necesario, lo cual es unicamente durante el primer render. 

Eso es lo que se llama ***lazy state initialization***. Es una optimización de performance. Es muy probable que no la tengas que usar frecuentemente. Pero es una técnica a tener en cuenta en tu tool box como React developer.