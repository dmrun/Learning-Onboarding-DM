Scope————————————————
Visibilidade de uma variável


Scope Chain—————————————

let a = 1;

function test() {
	let a = 11;
	console.log(a);
}
console.log(test());


Callbacks———————————————

function message(msg, callback) {
	console.log(msg)
       callback()
}


function endMessage() {
	console.log('end message')
}


message('hello world', endMessage);


- Passing function to other functions


setTimeout(endMessage, 3000)



Reference vs Value ……………………………………….

const a = [1];
const b = a;

a.push(2)
console.log(b)


Immutability ——————————————————



Type coercion —————————————————


- To String Coercion: string + number = string
Console.log(‘1’+2) = 12

- To Number Coercion: string (- * / %) number = number
Console.log(’12’-2) = 10

- To Boolean Coercion: true or false são convertidos para um número
console.log(true  +1) = 2
console.log(false  -1) =  -1



Arrow Functions ————————————————



const arrow1 = () => 3;

const arrow3 = () => {
  return 3
}

const arrow2 = () => ({
  nome: '11111'
});


console.log(arrow2());


const obj = {
  i: 10,
  b: () => console.log(this.i, this),
  c: function() {
    console.log(this.i, this);
  }
}


obj.b()





Short Circuits………………………………………………

&&   ||


Advanced Arrays methods…………………………..

const res = obj.map((el)=> {
	return {...el, stock: 0 }
})

const sum = obj.reduce((acc, cur) => {
	return acc + cur.price
}, 0);

Find, filter


spread operator

const res = obj.map((el)=> {
	return {...el, stock: 0 }
})

const arr1 = [1,2,3]
const arr2 = [4,5,6]
const arr = [...arr1, ...arr2];


Destructuring

const obj = {
	id: 1,
  name: 'my name'
};


Const { name } = obj;

// Delete the key name
const { name, ...rest } = obj;


Template Strings

const string1 = 'Hello';
const string2 = 'world';


const res = `${string1} ${string2}`;

console.log(res);


Async code: promises, async await


async function fetchMovies() {
  const response = await fetch(https://rickandmortyapi.com/api/episode/27);
  console.log(response);
}

fetch('http://example.com/movies.json')
  .then(response => response.json())



modules systems
