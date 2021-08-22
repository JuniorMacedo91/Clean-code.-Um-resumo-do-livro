[Página Principal](#clean-code-resumo-do-livro)

# Nomes significativos (variáveis, funções, classes)

Escolher um nome adequado é de extrema importância para entender seu propósito.

O nome de uma variável, função ou classe deve dizer:
  - Porque existe;
  - Como é usado; 
  - E o que faz;
 
Por esse motivo, evita-se comentários, pois se um nome não está claro, logo, não revela sua real necessidade.

## Variáveis

### Use nomes que revelem seu propósito.

:x:
```javascript
var y = 2002; 
```
Não sabemos se " y " é ano atual, ano de nascimento, entre outros.

:heavy_check_mark:
```javascript
var yearOfBirth = 2002; 
```
<hr>

### Evite informações erradas

Evite colocar nomes parecidos, nomes semelhantes a arquivos, documentos, atributos, tags, entre outros.

:x:
```javascript
var img = document.querySelector('#img1');  
```
Apesar de sabermos que " img " trata - se de alguma imagem, além de ser uma tag, não especifica sua real finalidade.

:heavy_check_mark:
```javascript
var homeBackgroundImage = document.querySelector('#img1'); 
```
<hr>

### Faça distinções

Faça a distinção dos nomes de uma forma que o leitor compreenda as diferenças, facilitando quando chama - las.

:x:
```javascript
var employee = '';
var employeerData = '';
var employeeInfo = '';
```
Qual das variáveis irá receber os dados do funcionário? E quais dados serão inseridos?

:heavy_check_mark:
```javascript
var employeeFullName = '';
var employeeDateOfBirth = '';
var employeeID = '';
```
<hr>

### Use nomes pronunciavés

Os nomes devem ser claros ao dizer

:x:
```javascript
var yyyy = new Date()
var year = yyyy.getFullYear()

```
:heavy_check_mark:
```javascript
const getCurrentYear = new Date()

var currentYear = yyyy.getFullYear()
```
<hr>

### Use nomes com facilidade para buscas

Devemos evitar nomes que usem apenas uma letra. Em carater de exceção, podemos usar dentro de um escopo local. Além do mais, o tamanho de um nome deve ser do tamanho do seu escopo.

:x:
```javascript
function calculate(number1,number2){
    let s = number1 + number2
    return s
}
```
:heavy_check_mark:
```javascript
function calculate(number1,number2){
    let sum = number1 + number2
    return sum
}
```
Apesar de ser um nome óbvio, é fácil de localizar.

<hr>

### Evite o mapeamento mental

A leitura de um nome deve ser fácil de se entender, sem a necessidade de traduzir mentalmente seu significado.

Isso acontece com nome de variáveis de uma letra só. Apesar de ser considerado um padrão, um contador de iteração ter nome como: i, j, k. De uma forma informal, deixa de ser uma variável para se tornar apenas um armazenador.

:x:
```javascript
function randomName(n){
if(n === something){
   return n
} else if( n === something){
   return n
}
...
...
...
...
}
```
Apesar da função ser sortear nome, " n " não especifica se será pelo nome mesmo, por algum número.

:heavy_check_mark:
```javascript
function randomName(name){
if(name === something){
   return name
} else if( name === something){
   return name
}
...
...
...
...
}
```
<hr>

## Classes e Objetos

Devem ter nomes de substantivos, evitando verbos.

:heavy_check_mark:
```javascript
const CAR = {
      name: 'Lamborghini Diablo',
      color: 'Black',
      year: '2019',
};
```
<hr>

## Funções

Os nomes das funções devem ser verbos. Sempre indicando o que será feito ao chama - las.
Também pode ser acrescidas de substantivos e métodos de acesso, alteração e autenticação como: GET, SET e IS.

:heavy_check_mark:
```javascript
function toCalculate(){
};

function getName(){    
}
```

:arrow_up:[Inicio](#nomes-significativos-variáveis-funções-classes)
