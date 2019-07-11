# Project 1: MDN Clone

Proyecto para aplicar lo aprendido hasta el momento de _HTML5, CSS3, JS (ES6+), Git y Metodologías ágiles_ :rocket:

A partir de este proyecto empezamos a trabajar utilizando _branches_ y [_Code Reviews_](https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/), siguiendo el [Feature Branch Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow) como metodología.

### Setup y Workflow

1) Deben trabajar en _un único repositorio_, creado por algún miembro del equipo, en el que el resto va a [colaborar](https://help.github.com/en/articles/inviting-collaborators-to-a-personal-repository). 

Ver el video [GITHUB PULL REQUEST, Branching, Merging & Team Workflow
](https://www.youtube.com/watch?v=oFYyTZwMyAg) para entender los detalles del flujo de trabajo.

2) Crear [_issues_](https://help.github.com/en/articles/about-issues) por cada feature que vayan a inplementar en el proyecto. Es recomendable agregar los issues al [_milestone_](https://help.github.com/en/articles/about-milestones) correspondiente, para trackear el progreso y poder estimar el tiempo para completarlo. También se aconseja utilizar los [_proyectos de GitHub_](https://help.github.com/en/articles/about-project-boards) para tener un tablero _Kanban_ donde se pueda visualizar el estado del proyecto en todo momento.

3) Cada miembro del equipo creará un _branch_ correspondiente a cada _feature_ y trabajará en ese branch (**:warning: no en master!**). Las features a implementar quedarán a criterio de cada equipo. La idea es intentar copiar, en lo posible el [_feature branch workflow_](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)

> :warning: En _master_ sólo tendremos código funcional y features completas (y revisadas por otros miembros del equipo, ver el punto 5 sobre _Code Reviews_)

4) Cuando el feature esté completo (y comiteado en el branch), debemos agregar el branch al repositorio remoto de GitHub: 

```git
git push --set-upstream origin <BRANCH_NAME>
```

5) Desde el repo en GitHub, crear un [_Pull Request_](https://help.github.com/en/articles/about-pull-requests). Asignárselo a otro miembro (ponerlo como [_reviewer_](https://help.github.com/en/articles/about-pull-request-reviews)) para que realice un [_Code review_](https://www.atlassian.com/agile/software-development/code-reviews) del mismo y eventualmente lo apruebe o proponga cambios y/o correcciones. A su vez, la persona que abra el _PR_ se pondrá como [_asignee_](https://help.github.com/en/articles/assigning-issues-and-pull-requests-to-other-github-users) y será la responsable de iterar sobre el feature (si es necesario hacer correcciones o cambios) hasta que llegue a _master_. **Esta instancia es fundamental**.

> 👉La idea es que **todos** los miembros del equipo haya hecho _al menos_ un PR y _al menos_ un Code Review

6) Luego de que el _PR_ sea aprobado y el correspondiente branch mergeado a _master_, ya podemos eliminar el branch, tanto de GitHub como de nuestro repo local, usando 

```git
git branch -d <BRANCH_NAME> // borra el branch local
git push origin --delete <BRANCH_NAME> // borra el branch remoto, es decir en Github. También podemos hacerlo desde GitHub 
git branch -D <BRANCH_NAME> // borra el branch local aunque no haya sido mergeado a master
```

> :warning: Recuerden _pullear_ los cambios de _master_ antes de _puhsear_ y arrancar una nueva feature!

7) Se aconseja (no es obligatorio) que algún miembro del equipo tome también el rol de _Project Manager_ para llevar un mejor control de las tareas y trabajar de forma más organizada.

8) Se aconseja también, en lo posible, juntarse en algún momento para agilizar el trabajo o usar alguna herramienta como Hangouts para tener calls.

9) Si necesitan repasar comandos de git, este es un buen [cheatsheet](https://github.com/joshnh/Git-Commands). Para repasar conceptos de git, se recomiendan los siguientes tutoriales:

- [Learn Git Branching](https://learngitbranching.js.org/)
- [Git Branch](https://www.atlassian.com/git/tutorials/using-branches)
- [Making a Pull Request](https://www.atlassian.com/git/tutorials/making-a-pull-request)
- [¿Por qué hacemos Code Reviews?](https://www.atlassian.com/agile/software-development/code-reviews)

## Sprint 1

### Implementar los siguientes métodos de arrays como funciones 

- [`forEach()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
- [`some()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
- [`every()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
- [`find()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
- [`includes()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)
- [`map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [`filter()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [`reduce()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

> ✨Se recomienda dejar `map()`, `filter()` y `reduce()` para el final, de manera que puedan reutilizar las funciones anteriores (por ejemplo, utilizar el `_forEach()` en la implementación del `_map()`).

1) Deben recibir al menos un array como parámetro y los parámetros extra necesarios (sólo los obligatorios, omitir los opcionales). Deben ser _funcionalmente iguales_ a los métodos originales, por lo que deben investigar bien qué hace cada uno.

Como convención para llamar a las funciones, vamos a usar el prefijo `_` seguido del nombre del método, usando _camelCase_. El _array_ debe ser el 1er parámetro de la función.

### Ejemplos: 

```js
_some(arr, fn)
_every(arr, fn)
_includes(arr, value)
```

**No pueden usar ningún método de la lista en la implementación de las funciones, pero sí reutilizar alguna función que definan ustedes en la implementación de otras.**

2) Todas las funciones deben definirse como _declaraciones_, en un archivo `app.js`

```js
...

function _some(arr, fn) {
  ...
}

function _every(arr, fn) {
  ...
}

function _includes(arr, value) {
  ...
}

...
```

3) Crear un `index.html`, _linkearlo_ al `app.js` mediante un tag `script`.

4) El `index.html` va a funcionar como _página de inicio_ de nuestro sitio, linkeando a las demás páginas. 

5) Además del `index`, tiene que haber una página de información para cada función, con el nombre correspondiente.

6) Como muestra el template, cada página deberá tener, al final, una sección _Ver también_, con enlaces para navegar a las otras páginas

7) Para la implementación de las funciones, utilizar lo visto en clase hasta el momento de JS.

### Ejemplos: 

```html
_some.html
_every.html
_includes.html
```

> Nota: Cada grupo decidirá cómo implementar cada página (elementos HTML y estilos). Los únicos requisitos son que la página de información de cada función contenga toda la información mostrada en el siguiente template de ejemplo y que se utilice _HTML5 semántico_. Será evaluada, como siempre, la aplicación de las [buenas prácticas](http://undefinedschool.io/best-practices/) (HTML, CSS y JS).

## Template

Las páginas de cada función deben contener toda la información que figura en este template (pueden agregar algún extra que consideren necesario)

![](https://i.imgur.com/iYHD9vs.png)

---

## Sprint 2

- Hacer las correcciones pedidas, post-evaluación.
- Implementar las acciones decididas por el grupo para mejorar la mecánica de trabajo, post-retro.
- Implementar el método [`_indexOf()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf) con un algoritmo _iterativo_, a través de la función `_indexOf`, con su correspondiente página `_indexOf.html`.
- Implementar el método [`_indexOfRecursive()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf) con un algoritmo _recursivo_, a través de la función `_indexOfRecursive`, con su correspondiente página `_indexOfRecursive.html`. Pista, utilizar [slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) ó [splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice) en la implementación.
- Utilizar `_forEach` en la implementación de `_map()` y `_filter()`.
- Utilizar `_indexOf` (versión iterativa) en la implementación de `_includes()`.
- Implementar el método [`_intersection()`](https://lodash.com/docs/4.17.11#intersection) (con su correspondiente HTML), que compara 2 arrays y retorna un nuevo array con los valores comunes a ambos.
- Implementar el método [`_union()`](https://lodash.com/docs/4.17.11#union) (con su correspondiente HTML), que compara 2 arrays y retorna un nuevo array con la unión de los valores de ambos, **sin repeticiones**. **Preservar el orden de los elementos, comenzando desde el primer elemento del primer array pasado por parámetro**.
- Implementar el método [`_sum()`](https://lodash.com/docs/4.17.11#sum) (con su correspondiente HTML), utilizando `_reduce` en su implementación, que recibe un array de números y retorna la suma de todos sus valores. 
- Agregar al `index.html` y a la sección _Ver también_ de cada página enlaces a las nuevas funciones.

### Repaso de recursión

- [Algorithms: Recursion](https://www.youtube.com/watch?v=KEEKn7Me-ms).
- [Recursion Crash Course](https://www.youtube.com/watch?v=lMBVwYrmFZQ).
- [Understanding Recursion: A JavaScript Example](https://www.youtube.com/watch?v=py7ZWFjrwEs).
- Resolver un problema mediante recursión significa que la solución depende de las soluciones de pequeñas instancias (subproblemas) del mismo problema.
- Necesitamos: **caso base** y **caso recursivo**.
- **Todo algoritmo recursivo debe tener al menos un caso base, sino nunca va a terminar!**.
- Aparte del **caso base**, para asegurarnos de que enventualmente llegamos a él, **cada llamada recursiva debe ser invocada con una instancia más simple (y diferente) del problema**.
- Ejemplo: [Sucesión de Fibonacci](https://es.wikipedia.org/wiki/Sucesi%C3%B3n_de_Fibonacci).
- **Cualquier algoritmo recursivo puede escribirse de forma _iterativa_**. Es parte de las optimizaciones que aplica el compilador.
- Los algoritmos recursivos suelen ser _ineficientes_. Se los utiliza en casos simples (porque suelen ser más legibles), siempre que sepamos que no vamos a _reventar el stack_. :bomb::boom:

---

## Sprint 3

- Agregar el parámetro `initialValue` al `_reduce()`. Modificar, si es necesario, el código de la función para que lo utilice y actualizar su HTML.
- Implementar el método [`_min()`](https://lodash.com/docs/4.17.11#min), que retorna el valor mínimo de un array. El array puede ser de `number`ó `string`. 
  - `_min([4, -1, 10, 127]) => -1`.
  - `_min(['a', '1', 'j']) => 1`. 
  - Si es vacío, retornar `undefined`.
- Implementar el método [`_max()`](https://lodash.com/docs/4.17.11#max) (con su correspondiente HTML), que retorna el valor máximo de un array. El array puede ser de `number`ó `string`. 
  - `_max([4, -1, 10, 127]) => 127`.
  - `_max(['a', '1', 'j']) => 'j'`. 
  - Si es vacío, retornar `undefined`.
- Usar el tag semántico [`<code>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code) para las secciones de código. Tener en cuenta que `code` es _inline_, por lo que quizás sea necesario utilizarlo junto con [`pre`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre) para que el código mantenga su forma.
- Agregar al `index.html` y a la sección _Ver también_ de cada página los enlaces correspondientes a las nuevas funciones.
- Investigar cómo usar [`highlight.js`](https://highlightjs.org/) e implementarlo en las secciones de código JavaScript, para resaltar la sintaxis.

## Sprint 4

- Implementar el método [`_findIndex()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex) (con su correspondiente HTML).
- Implementar el método [`_lastIndexOf()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf) (con su correspondiente HTML).
- Implementar el método [`_concat()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat) (con su correspondiente HTML).
- Implementar el método `_isEqual()`, que redibe 2 arrays (unidimensionales) como parámetro y retorna `true` si son iguales (es decir, tienen los mismos elementos y en el mismo orden) ó `false`en caso contrario (con su correspondiente HTML).
- Agregar al `index.html` y a la sección _Ver también_ de cada página los enlaces correspondientes a las nuevas funciones.

## Sprint 5

En este sprint no hay nuevas features para implementar, sino básicamente pulir la base que tenemos para las próximas etapas

- Prestarle más atención al maquetado
- Hacer las correcciones pendientes
- Cerrar PRs colgados, conflictos, etc

## Sprint 6

- Renombrar los métodos implementados con el prefijo `_` en lugar de `fake`
- Renombrar los métodos `fakeArrayMax()` y `fakeArrayMin()` como `_max()` y `_min()` respectivamente 
- Renombrar el método `areEqual()` como `_isEqual()`, por consistencia con el [nombre original](https://lodash.com/docs/4.17.11#isEqual)
- Hacer las correcciones pendientes
- Cerrar PRs colgados, conflictos, etc
- Validar el [HTML](https://validator.w3.org/) y el [CSS](https://jigsaw.w3.org/css-validator/) que utilizamos

## Sprint 7

- Reescribir las funciones como métodos de _Array_, usando el [prototype](https://eloquentjavascript.net/06_object.html#h_SumMlRB7yn)
- Adaptar la documentación (sintaxis, ejemplos, etc) donde corresponda
