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

#### split()
Separa os caracteres de uma String em um Array
```
const nome = 'Emmanuel';
nome.split('');

Saída: ["E", "m", "m", "a", "n", "u", "e", "l"];
```

#### reverse();
Inverte a ordem de colocação de items em um Array
```
const array = ['a','b','c'];
array.reverse();

Saída: ['c','b','a'];
```

#### join()
Une items de um Array para formar uma string
```
const nome = 'Emmanuel';
nome.split('').reverse.join();

Saída: "l,e,u,n,a,m,m,E"
Para remover as vírgulas e tornar uma String sem espaços basta passar como parâmetro para o join('') uma string vazia:
Saída: "leunammE";
```
#### Math.sign()
1. Retorna 1 se número é positivo
2. Retorna -1 se número é negativo
3. Retorna 0 se número é nulo = 0;
4. Funciona com string '1111' ou '-1111' mas retorna NaN para letras.
```
console.log(Math.sign(51))
// Saída: 1

console.log(Math.sign(-36))
// Saída: -1

console.log(Math.sign(0))
// Saída: 0
```
#### Math.sqrt()
1. Retorna a raiz quadrada do número
```
console.log(Math.sqrt(90))

// Saída: 9.486832980505138
```
#### Math.sin()
1. Retorna o seno de um numero
```
console.log(Math.sin(4))
// Saída: -0.7568024953079282
```
#### Math.floor() + Math.random
1. floor() retorna um número inteiro.
2. random() gera um número aleatório.
3. Usados em conjunto é possível randomizar geração de números inteiros aleatórios entre um intervalo.
```
console.log(Math.floor(Math.random() * 10));

// Saída: um número aleatório de 0 à 10.

console.log(Math.floor(Math.random() * 10) + 1);

// Saída: um número aleatório de 1 à 10.
```
#### Math.max() / Math.min()
1. Retorna valor máximo e mínimo respectivamente.
```
console.log(Math.max(4, 1550, 110, 28, -71, -752))

// Saída: 1550

const a = [1,0,-5,7,12]
console.log(Math.max(...a));

// Saída: 12
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
### Fontes responsivas usando calc()

- largura máxima das páginas: 1200px,
- breakpoint para fontes: 500px,
- tamanhos das fontes:
- viewport < 500px — font-size: 16px;
- viewport > 500px — font-size: 24px;
- Para viewport maior que 500px tamanho da fonte deverá variar de 16px até 24px ou seja uma variação de 8px.
- A taxa de variação do tamanho da fonte é de 8/1200 = 0,66667%
- Para viewport maior que 500px devemos declarar um tamanho de fonte igual a: calc(16px + 0.6667vw)
- font-size = calc( [font-size-min] + ( ([font-size-max] - [font-size-min]) / [max-width-pag] ) * 100vw
```
@media screen and (min-width: 500px) {
  .texto {
    font-size: calc(16px + (8/1200) * 100 * 1vw);
  }
}
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
- 0 não é primo pois pode ser dividido por qualquer outro número;
- 1 não é primo pois só possui um divisor (ele mesmo = 1);
- então começamos a partir do 2.
```
function exibePrimos(limite){
    for(let i=2; i<=limite; i++){
        ehPrimo(i) &&
           console.log(i);
    }
}

function ehPrimo(value){
    for(let j=2; j<value; j++){
        if(value%j === 0){
            return false;
        }
    }
    return true;
}
```
format price
```
create arquive parseMoney:

const formatter = new Intl.NumberFormat('pt-BR', {
	style: 'currency',
	currency: 'BRL'
});

export default function(number) {
	return formatter.format(number);
}


Usage import:
import parseMoney from 'parseMoney';

parseMoney(value);
```
