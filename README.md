# codes

### js
#### sort()
Para comparar números ao invés de texto, a função de comparação pode simplesmente subtrair b de a. A função abaixo irá ordenar o array em ordem crescente:

```
function compararNumeros(a, b) {
  return a - b;
}
```

O método de ordenação pode convenientemente ser usada com funções anônimas (e closures):

```
var numbers = [4, 2, 5, 1, 3];
numbers.sort(function(a, b) {
  return a - b;
});

console.log(numbers);
```

#### concat()
Concatena arrays ou valores criando um novo array sem alterar os arrays originais.

```
Exemplos 01
var alpha = ["a", "b", "c"];
var numeric = [1, 2, 3];

// creates array ["a", "b", "c", 1, 2, 3]; alpha and numeric are unchanged
var alphaNumeric = alpha.concat(numeric);
```
```
Exemplo 02
O código a seguir une três arrays:

var num1 = [1, 2, 3];
var num2 = [4, 5, 6];
var num3 = [7, 8, 9];

// creates array [1, 2, 3, 4, 5, 6, 7, 8, 9]; num1, num2, num3 are unchanged
var nums = num1.concat(num2, num3);
```

#### slice()
Retorna uma cópia de parte de um array a partir de um subarray criado entre as posições início(begin) e fim(end)(não necessário especificar caso deseje ir até o final do array e não parando antes) de um array original.

- slice(1,4) extrai do segundo até o quarto elemento (elementos de índice 1, 2 e 3).
```
// Exemplo extrair nossos bons amigos, os cítricos, das frutas
var frutas = ['Banana', 'Laranja', 'Limao', 'Maçã', 'Manga'];
var citricos = frutas.slice(1, 3);

// citricos contem ['Laranja','Limao']
```

#### filter()
Cria um novo array com todos os elementos que obedeçam a condição fornecida.
```
Exemplo 01
function isBigEnough(value) {
  return value >= 10;
}

const filtered = [12, 5, 8, 130, 44].filter(isBigEnough);
// filtrado é [12, 130, 44]
```
```
Exemplo 02
const array = ['Matheus','Julia','Thiago'];

const filtered = array.filter(item => item === 'Matheus');

// Saída esperada: ['Matheus']
console.log(filtered)
```

#### map()
Mapeia o array devolvendo um novo array como resultado.
```
const array = [1,2,3,4,5,6,7,8,10];

const newArray = array.map(item => item*2);

// Saída esperada: [2, 4, 6, 8, 10, 12, 14, 16, 20]
console.log(newArray);
```

#### reduce()
Executa uma função de redução (fornecida por você) para cada elemento do array, resultando um valor único para retorno.

```
const array = [1,2,3,4,5,6,7,8,10];

const reduceArray = array.reduce((increment, current) => increment + current);

// Saída esperada: 46 (soma dos valores do array)
console.log(reduceArray);
```

#### some()
Testa se algum dos elementos no array obedecem à condição implementada pela função atribuída.

- Retorna true se pelo menos um dos elementos obedecer;
- Retorna false se nenhum dos elementos obedecerem;
```
O exemplo a seguir testa se algum elemento de um array é maior que 10.

function isBiggerThan10(element, index, array) {
  return element > 10;
}
[2, 5, 8, 1, 4].some(isBiggerThan10);  // false
[12, 5, 8, 1, 4].some(isBiggerThan10); // true
```
```
Exemplo 02
const array = [2,4,8,10];

const someResult = array.some((item) => item > 10);

// Saída esperada: true;
console.log(someResult);
```
#### find()
Retorna o valor do primeiro elemento do array que satisfizer a função de teste provida. Caso contrario, undefined é retornado.
```
const array = ['Joao','Caio','Joao','Thiago','Maria','Sofia'];

const findPeople = array.find(item => item === 'Joao');

// Saída esperada: "João"
console.log(findPeople);
```

### css
scroll suave por âncoras
```
html {
  scroll-behavior: smooth;
}
```
texto com imagem ou vídeo de fundo
```
-webkit-background-clip: text; 
  // adiciona um clip de linear gradient do elemento por tras, dentro do texto;
-webkit-text-fill-color: transparent; 
  // remove a cor de preenchimento do texto permitindo ver o degrade dentro do texto.
display: inline; 
  // para o background n ocupar 100% width enquanto o texto apenas uma parte.
  
  ------ ou
  position: absolute; na div principal, no vídeo e no texto +
  texto{
  	background: color;
	color: color;
	mix-blend-mode: screen;
  }
```
aplicando gradient em cima de imagens pelo css
```
background: url(img.jpg), linear-gradient(230deg, cor1, cor2);
background-blend-mode: luminosity;
```
meus tamanhos para responsividade
```
@media screen and (max-width: 960px/768px/480px){
     
}
```
efeito mesclagem entre imagem principal e section inferior
```
1. Criar pseudo elemento:

sectionatual::after {
background: linear-gradient(0deg,#130b1a 0,rgba(19,11,26,.71) 
  22%,rgba(19,11,26,.66) 
  38%,rgba(7,6,10,.61) 
  58%,rgba(11,7,21,.76) 100%);
}

2. A primeira cor é a da seção de baixo, as demais são variações para formar degrade
setar a bg do elemento original com position absolute;
```



### jquery
scroll suave
```
$('.nav a[href^="#"]').on('click', function(e) {
	e.preventDefault();
	var id = $(this).attr('href'),
			targetOffset = $(id).offset().top;
			
	$('html, body').animate({ 
		scrollTop: targetOffset - 100
	}, 600);
});
```




### git
corrigir mensagem de commit
```
git commit -m "mensagem corrigida" --amend
```
apagar um commit contando para trás
```
git reset --soft HEAD~(quantidade de commits)
ou
git rebase -i HEAD~(quantidade de commits)
```
remover um arquivo antes colocado no estado com git add
```
git reset -- NOME DO ARQUIVO
```
removendo mais de um arquivo antes colocado no estado com git add
```
1. git add -i
2. opção 3 para reverter
3. digitar número dos arquivos para remoção + enter
```




### regex
renomear todos os arquivos de um diretório que possuam a extensão configurada
```
rename 's/\.JPG/\.jpg/' *.JPG
```




### links
cdn fontawesome -> 
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css">









### trechos de código
Exibir números primos até um certo valor:
```
function exibePrimos(limite){
let primos = [];
    for(let i=1; i<limite; i++){
        const numero = ehPrimo(i);
        primos = [...primos, numero];
    }
    console.log(primos);
}

function ehPrimo(value){
    for(let i=1; i<value; i++){
        if(value%i !== 0){
            return value;
        }
    }
}
```

