# Learning

O presente documento descreve a aprendizagem adquirida não só sobre Javascript mas também sobre React no âmbito do meu onboarding (Daniel Mateus).

## Abordagem Inicial - React App

De modo a criar a primeira app em React, devem ser inseridos os seguintes comandos:

    npx create-react-app my-app
    cd my-app
    npm start

_There are two types of “model” data in React: props and state. The two are very different_:

- _Props are like arguments you pass to a function. They let a parent component pass data to a child component and customize its appearance. For example, a Form can pass a color prop to a Button_.
- _State is like a component’s memory. It lets a component keep track of some information and change it in response to interactions. For example, a Button might keep track of isHovered state_.

Exemplos de componentes React:

    //Title Component
    const Title = ({ text }) => {
        return (
            <>
                <h2>{text}</h2>
            </>
        );
    };

    export default Title;

    //Image Component
    const Image = (props) => {
        return (
            <>
                <img src={props.src} className={props.className} alt={props.alt} />
            </>
        );
    };

    export default Image;

## Free Code Camp - Learning

O free code camp foi utilizado durante este onboarding de modo a recordar e consolidar conceitos de [Javascript](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/). Desta forma, e para referências futuras, os módulos mais relevantes foram:

1. Basic JavaScript
2. ES6
3. Debugging
4. Basic Data Structures
5. Functional Programming

Por sua vez, os módulos do curso opcionais são:

1. Regular Expressions
2. Basic Algorithm Scripting
3. Object Oriented Programming
4. Intermediate Algorithm Scripting
5. JavaScript Algorithms and Data Structures Projects

## Conceitos a reter

### Teoria

A seguinte informação espelha alguns pontos que considerei relevantes, tanto do curso (freecodecamp - Javascript) como de self-research.

_JavaScript provides eight different **data types** which are undefined, null, boolean, string, symbol, bigint, number, and object._

**_Var and Let_** _are both used for variable declaration in javascript but the difference between them is that var is function scoped and let is block scoped. It can be said that a variable declared with var is defined throughout the program as compared to let. An example will clarify the difference even better._

_In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code._

_Functional programming is about:_

1. _Isolated functions - there is no dependence on the state of the program, which includes global variables that are subject to change._

2. _Pure functions - the same input always gives the same output._

3. _Functions with limited side effects - any changes, or mutations, to the state of the program outside the function are carefully controlled._

4. _Callbacks are the functions that are slipped or passed into another function to decide the invocation of that function. You may have seen them passed to other methods, for example in filter, the callback function tells JavaScript the criteria for how to filter an array._

   1. _Functions that can be assigned to a variable, passed into another function, or returned from another function just like any other normal value, are called first class functions. In JavaScript, all functions are first class functions._
   2. _The functions that take a function as an argument, or return a function as a return value are called higher order functions._
   3. _When functions are passed in to or returned from another function, then those functions which were passed in or returned can be called a lambda._

<br>

_The **slice** method returns a copy of certain elements of an array._

_A common pattern while working with arrays is when you want to remove items and keep the rest of the array. JavaScript offers the **splice** method for this, which takes arguments for the index of where to start removing items, then the number of items to remove. If the second argument is not provided, the default is to remove items through the end. However, the splice method mutates the original array it is called on._

_Array.prototype.reduce(), or simply **reduce()**, is the most general of all array operations in JavaScript. You can solve almost any array processing problem using the reduce method._

_The reduce method allows for more general forms of array processing, and it's possible to show that both filter and map can be derived as special applications of reduce. The reduce method iterates over each item in an array and returns a single value (i.e. string, number, object, array). This is achieved via a callback function that is called on each iteration._

_The callback function accepts four arguments. The first argument is known as the accumulator, which gets assigned the return value of the callback function from the previous iteration, the second is the current element being processed, the third is the index of that element and the fourth is the array upon which **reduce** is called.
In addition to the callback function, reduce has an additional parameter which takes an initial value for the accumulator. If this second parameter is not used, then the first iteration is skipped and the second iteration gets passed the first element of the array as the accumulator._

### Prática

Exemplo Reduce:

    const users = [
      { name: 'John', age: 34 },
      { name: 'Amy', age: 20 },
      { name: 'camperCat', age: 10 }
    ];

    const sumOfAges = users.reduce((sum, user) => sum + user.age, 0);
    console.log(sumOfAges);
    //The console would display the value 64.

Exemplo reduce a retornar um objeto:

    const users = [
      { name: 'John', age: 34 },
      { name: 'Amy', age: 20 },
      { name: 'camperCat', age: 10 }
    ];

    const usersObj = users.reduce((obj, user) => {
        obj[user.name] = user.age;
        return obj;
    }, {});

    console.log(usersObj);
    //The console would display the value { John: 34, Amy: 20, camperCat: 10 }

## README file (Markdown)

Segue o exemplo de README file criado para o projeto [Ninja Profile](https://github.com/dmrun/onboarding-css-react-multipage-app):

[README.md](https://github.com/dmrun/onboarding-css-react-multipage-app/blob/master/README.md)

Este ficheiro foi criado com base nos princípios e conteúdos das seguintes fontes:

[Basic Syntax | Markdown](https://www.markdownguide.org/basic-syntax/#line-breaks)

[How to Write a Good README File](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/)

## Referências

1. [React Docs Beta](https://beta.reactjs.org/learn)
2. https://code.visualstudio.com/docs/nodejs/reactjs-tutorial
3. https://gist.github.com/rachelnabors/c64b3aeace8a191cf5ea6fb5202e66c9
4. https://reactjs.org/tutorial/tutorial.html
5. https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/
6. https://www.markdownguide.org/basic-syntax/
7. https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/
8. https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/

## Anexo

javascript.md : Ficheiro com exemplos práticos de alguns dos temas abordados.
