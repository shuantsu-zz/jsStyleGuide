# Manual de instação do ESLint para garantir o uso das regras de estilo Javascript da Airbnb :fa-file-text-o:

### Requisitos :fa-check-square-o:

- Extensão Eslint instalada no VSCode https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

- Explicação das regras de estilo:
https://github.com/airbnb/javascript

------------

### Passo a passo :fa-list-ol:

(Baseado em: https://dev.to/devdammak/setting-up-eslint-in-your-javascript-project-with-vs-code-2amf)

1. `mkdir pastaProjeto && cd pastaProjeto`
2. `npm init --yes`
3. `npm install eslint -g`
4. `eslint --init`
5. Será apresentado um questionário. Sugestão de preenchimento:

**How would you like to use ESLint?**
To check syntax, find problems, and enforce code style

**What type of modules does your project use?**
CommonJS (require/exports)

**Which framework does your project use?**
*Responder de acordo com requerimentos do projeto*

**Where does your code run?**
Browser

**How would you like to define a style for your project?**
Use a popular style guide

**Which style guide do you want to follow?**
Airbnb

**What format do you want your config file to be in?**
Javascript

**Would you like to install them now with npm?**
Yes

Você deverá então ter um arquivo `.eslintrc.js` na raiz, semelhante a este:

```java
module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es2020: true,
  },
  extends: [
    'airbnb-base',
  ],
  parserOptions: {
    ecmaVersion: 11,
  },
  rules: {
    'no-console': 'off',
  },
};

```

- **Perceba na linha 14 a inclusão feita manualmente da regra no-console: off**
Isso permite que se use o objeto console, algo que não é padrão desse guia de estilo. Apenas lembre-se de remover os logs ao mandar para produção.

------------

### Configurações do VSCode :fa-gear:

Talvez seja necessário fazer pequenas configurações no VSCode que não vem por padrão.
(Para configurar vá em Configurações no VSCode ou pressione Ctrl + vírgula.)

- A tabulação deverá inserir dois espaços ao invés de 4.
-> Usando a busca, desabilite a opção **Detect Indentation** e mude **Tab size** para `2`.

- O fim de linha deve ser `\n` e não `\r\n`.
-> Usando a busca, mude a opção **files.eol** para `\n`

------------

Com todas as configurações feitas, você verá um sublinhado em vermelho no trecho que está em conflito com as normas de estilo. Passe o mouse em cima do trecho para ver a classificação do erro, e a documentação relacionada ao erro será  mostrada.