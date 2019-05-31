# Project 1: fakeMDN

Este es el proyecto 1, para aplicar lo aprendido hasta el momento de _HTML5, CSS3, JS (ES6+), Git y Metodologías ágiles_ :rocket:

A partir de este proyecto empezamos a trabajar utilizando _branches_ y [_Code Reviews_](https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/)

## Parte 1

## Setup y Workflow

1) Deben trabajar en _un único repositorio_, creado por algún miembro del equipo, en el que el resto va a colaborar. 

Ver el video [GITHUB PULL REQUEST, Branching, Merging & Team Workflow
](https://www.youtube.com/watch?v=oFYyTZwMyAg) para entender los detalles del flujo de trabajo.

2) Crear [_issues_](https://help.github.com/en/articles/about-issues) por cada feature que vayan a inplementar en el proyecto. Es recomendable agregar los issues al [_milestone_](https://help.github.com/en/articles/about-milestones) correspondiente, para trackear el progreso y poder estimar el tiempo para completarlo. También se aconseja utilizar los [_proyectos de GitHub_](https://help.github.com/en/articles/about-project-boards) para tener un tablero _Kanban_ donde se pueda visualizar el estado del proyecto en todo momento.

3) Cada miembro del equipo creará un _branch_ correspondiente a cada _feature_ y trabajará en ese branch (**:warning: no en master!**). Las features a implementar quedarán a criterio de cada equipo. La idea es intentar copiar, en lo posible el [_feature branch workflow_](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)

4) Cuando el feature esté completo (y comiteado en el branch), debemos agregar el branch al repositorio remoto de GitHub: 

```git
git push --set-upstream origin <BRANCH_NAME>
```

5) Desde el repo en GitHub, crear un [_Pull Request_](https://help.github.com/en/articles/about-pull-requests). Asignárselo a otro miembro (ponerlo como [_reviewer_](https://help.github.com/en/articles/about-pull-request-reviews)) para que realice un [_Code review_](https://www.atlassian.com/agile/software-development/code-reviews) del mismo y eventualmente lo apruebe o proponga cambios y/o correcciones. **Esta instancia es fundamental**.

6) Luego de que el _PR_ sea aprobado y el correspondiente branch mergeado a _master_, ya podemos eliminar el branch, tanto de GitHub como de nuestro repo local, usando 

```git
git branch -d <BRANCH_NAME> // borra el branch local
git branch -D <BRANCH_NAME> // borra el branch de GitHub. También podemos hacerlo desde GitHub
```

7) Se aconseja (no es obligatorio) que algún miembro del equipo tome también el rol de _Project Manager_ para llevar un mejor control de las tareas y trabajar de forma más organizada.

8) Se aconseja también, en lo posible, juntarse en algún momento para agilizar el trabajo o usar alguna herramienta como Hangouts para tener calls.

9) Si necesitan repasar comandos de git, este es un buen [cheatsheet](https://github.com/joshnh/Git-Commands). Para repasar conceptos de git, se recomiendan los siguientes tutoriales:

- [Learn Git Branching](https://learngitbranching.js.org/)
- [Git Branch](https://www.atlassian.com/git/tutorials/using-branches)
- [Making a Pull Request](https://www.atlassian.com/git/tutorials/making-a-pull-request)
- [¿Por qué hacemos Code Reviews?](https://www.atlassian.com/agile/software-development/code-reviews)

## Implementar los siguientes métodos de arrays como funciones 

- [`forEach`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
- [`some`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
- [`every`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
- [`find`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
- [`includes`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)
- [`map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [`filter`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [`reduce`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

1) Deben recibir al menos un array como parámetro y los parámetros extra necesarios (sólo los obligatorios, omitir los opcionales). Deben ser _funcionalmente iguales_ a los métodos originales, por lo que deben investigar bien qué hace cada uno.

Como convención para llamar a las funciones, vamos a usar el prefijo _fake_ seguido del nombre del método, usando _camelCase_. El _array_ debe ser el 1er parámetro de la función.

### Ejemplos: 

```js
fakeSome(arr, fn)
fakeEvery(arr, fn)
fakeIncludes(arr, value)
```

**No pueden usar ningún método de la lista en la implementación de las funciones, pero sí reutilizar alguna función que definan ustedes en la implementación de otras.**

2) Todas las funciones deben definirse como _declaraciones_, en un archivo `app.js`

```js
...

function fakeSome(arr, fn) {
  ...
}

function fakeEvery(arr, fn) {
  ...
}

function fakeIncludes(arr, value) {
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
fakeSome.html
fakeEvery.html
fakeIncludes.html
```

> Nota: Cada grupo decidirá cómo implementar cada página (elementos HTML y estilos). Los únicos requisitos son que la página de información de cada función contenga toda la información mostrada en el siguiente template de ejemplo y que se utilice _HTML5 semántico_. Será evaluada, como siempre, la aplicación de las [buenas prácticas](http://undefinedschool.io/best-practices/) (HTML, CSS y JS).

## Template

Las páginas de cada función deben contener toda la información que figura en este template (pueden agregar algún extra que consideren necesario)

![](https://i.imgur.com/iYHD9vs.png)
