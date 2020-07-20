# Guia de estilo de JavaScript - Algumas regras básicas
Baseado em: https://www.robinwieruch.de/javascript-naming-conventions

## Como declarar uma variável

“const” para uma variável que não será redeclarada
“let” para variável que poderá ser redeclarada.

## Convenção para nome de variável

Variáveis devem estar em inglês e no padrão “camelCase”.

### Exemplos:

firstName
moneyAmount
ageSum

Etc…

##Posição da declaração de variável

Não posição mais ao topo possível do escopo.

## Nome de variáveis booleanas

Variáveis de tipo booleano definem se algo é verdadeiro ou falso, e devem ser precedidas por prefixos como “is”, “are” ou “has”.

Exemplos:

// bad
const visible = true;
 // good
const isVisible = true;
 // bad
const equal = false;
 // good
const areEqual = false;
 // bad
const encryption = true;
 // good
const hasEncryption = true;


## Nome de funções e métodos

Funções ou métodos devem ser precedidas por verbos que descrevem o que ela faz.

Exemplos:

fetchUserData
postNewBlogEntry
calculateSquareRoot
applyActiveState

Etc…

## Definição de classes e componentes

Padrão Pascal:

UserProfile
BlogPost
ContactForm

## Ponto e vírgula

Sempre usar ponto e vírgula no final da linha para evitar bugs introduzidos pelo insersor automático de ponto e vírgula do javascript, que pode variar de comportamento ao passo que a linguagem ganha novas regras.

Explicação: https://github.com/airbnb/javascript#semicolons

## Controle de fluxo (if, elseif, else)

Sempre usar chaves mesmo que uma única expressão seja usada, para facilitar a compreensão, evitar bugs e melhorar a manutenção.