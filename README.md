<h1 align="center">
    <img src="./img/img000.png" />
</h1>

# ignite-react-chapter02
## Chapter II 

## Trilha ReactJS 

## Primeira Aplicação Web com ReactJS

### 1 Estrutura da aplicação

### 1.1 Introdução do módulo

### 1.2 Estrutura com create-react-app

Vamos cria um template que ira monta toda a base de uma aplicação:
`yarn create react-app ignite-react-chapter02 --template typescript`

Agora vamos limpar o projeto:
Vamos inicia pelo arquivo: public/index.html

Vamos retira:
`<link rel="icon" href="%PUBLIC_URL%/favicon.ico" />`

E vou retira tudo ate o title

<h1 align="center">
    <img src="./img/img001.png" />
</h1>

Vamos trocar o titulo de `<title>React App</title>` para `<title>Controle Contábil</title>`:

Vamos deletar toda parte comentada a baixo e ficara assim:

<h1 align="center">
    <img src="./img/img002.png" />
</h1>

E vamos deletar todos os arquivos da pasta `public` menos o arquivo `index.html`.

<h1 align="center">
    <img src="./img/img003.png" />
</h1>

E dentro da pasta `src` vamos delatar os arquivos:

<h1 align="center">
    <img src="./img/img004.png" />
</h1>

Ficando so o arquivos: `App.tsx`, `index.tsx` e `react-app-env.d.ts`.

No `index.tsx` vamos remover a importação do css `import './index.css';`.
A importação do `import reportWebVitals from './reportWebVitals';`.
E toda parte comentada.

No `App.tsx` vamos remover a importação do `import React from 'react';`.
A importação do `import logo from './logo.svg';`.
A importação do `import './App.css';`.

Retira todo o `header`. e deixa so a div.

E vamos colocar um `<h1>Hello World</h1>`

E vamos tambem expostar o App `export function App() {}`

Assim que importa a `App` so vai poder importa com nome `App`. Isso vai ajudar a debugar o codigo.

Agora dentro do aquivo `package.json` vamos criar uma `"devDependencies"` recortando os codigos e colocando nele.

<h1 align="center">
    <img src="./img/img005.png" />
</h1>

### 1.3 Exportando assets do Figma

Link para acessa figma:
https://www.figma.com/file/0xmu9mj2TJYoIOubBFWsk5/dtmoney-Ignite-(Copy)?node-id=0%3A1

Caso não consiga baixar pelo figma segui o link das logos.
E link Assets:
https://xesque.rocketseat.dev/platform/1615808314498-attachment.zip

Vamos exportar as `layers` que significa camadas: 
1 - Logo.

<h1 align="center">
    <img src="./img/img006.png" />
</h1>

Vamos criar uma pasta dentro `src` com o nome de `assets` e colocar logos.
Esse vamos reomea para `logo.svg`.

2 - Vamos exposta so a bolinha:
no formado png
E vou chamar de `favicon.png`
Na pasta index.html

<h1 align="center">
    <img src="./img/img007.png" />
</h1>

3 - Agora os vetores
no formado svg

<h1 align="center">
    <img src="./img/img008.png" />
</h1>

4 - o vetor de fecha

Ficando assim:

<h1 align="center">
    <img src="./img/img009.png" />
</h1>

E vamos anotar as cores do figma para passar no scc:

