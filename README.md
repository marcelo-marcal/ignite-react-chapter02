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

4 - O vetor de fecha

E ficando assim os vetores renomeados:

<h1 align="center">
    <img src="./img/img009.png" />
</h1>

E vamos anotar as cores do figma para passar no scc:

### Instalando Styled Components

Vamos inicia instalando uma das bibliotecas que e Styled Components

`yarn add styled-components`

Vamos no arquivo `App.tsx` entender nossa estilização.

Vamos entender com esse Exemplo:
E vamos cria um `App.css` e vamos estilizar uma propriedade `.title`

<h1 align="center">
    <img src="./img/img010.png" />
</h1>

E vamos em `App.tsx` importamos o `App.css`.
e vamos colocar um `className` dentro do `h1` assim `<h1 className="title">Hello World</h1>`.

<h1 align="center">
    <img src="./img/img011.png" />
</h1>

E vamos rodar a aplicação com:
`yarn start`

localhost:3000
<h1 align="center">
    <img src="./img/img012.png" />
</h1>

Agora vamos fazer diferente:
Vamos apaga o arquivo `App.css` e dentro do arquivo `App.tsx` vamos importa:
`import styled from 'styled-components';` e ele ira apresenta um erro:

<h1 align="center">
    <img src="./img/img013.png" />
</h1>

E sempre que aparecer esse tipo de error que sugere instala um pacote adicional, nos instalamos como dependencia de desenvolvimento.
`yarn add @types/styled-components -D`

E para estiliza o mesmo titulo usando Styled Components.
Vamos criar um componente estilizado, como uma costante variavel chamada por exemplo `Title` ficando assim:

`const Title = styled.h1`` `
Instala a extenção do VC.Code `vscode-styled-components`.

E ao em vez de colocar `h1` vamos colocar um componete `title`

<h1 align="center">
    <img src="./img/img014.png" />
</h1>

Tendo a vantagem do css ficar proximo e não atralha os outros css de componetes.

### Criando estilos globais

Como usar Styled Components, para criar umas estilizações globais para a aplicação.
Vamos começa remomvendo tudo que tem do Styled Components dentro do `App.tsx`.

```
import styled from 'styled-components';

const Title = styled.h1`
  font-size: 64px;
  color: #8257e6;
`
```
Vamos deixa so o h1 com Hello World `<h1>Hello World</h1>` dentro da div.

E dentro da pasta `public` no arquivo `index.html` colocar nosso favicon.

<h1 align="center">
    <img src="./img/img015.png" />
</h1>

E vamos rodar a aplicação com:
`yarn start`

Agora para fazer os estilos globais vamos na pasta `src` vamos criar uma pasta `styles` e dentro dela um arquivo `global.ts`.
Vamos criar um a importação: `import { createGlobalStyle } from 'styled-components';`
E criar uma variavel: `export const GlobalStyle = createGlobalStyle`` ` com spas no final para colocamos os codigo css.

Seve para deixa a fonte com mais qualidade nos Browser `-webkit-font-smoothing: antialiased;`.

<h1 align="center">
    <img src="./img/img016.png" />
</h1>

Agora vamos importa o arquivo para ver como ele esta:

No arquivo `App.tsx` que e o arquivo principal da aplicação vamos colocar o `<GlobalStyle/>` em qualque lugar e depois arrumamos.

E vamos continual no arquivo `global.ts`.
E configura o tamanho de fonte da aplicação. E por pagrão o font-size: 16px e um padrão e fuciona muito bem para Desktop.

Eu vou falar quando meu usuario estive com uma tela ate 1080px de largura, eu vou diminuir o font-size eu vou deixa ele em 93.75%.
Isso para quando a aplicação for usada em dispositivos menores.

<h1 align="center">
    <img src="./img/img017.png" />
</h1>

Vamos continuar estilzando.
Um `cursor: pointer;` dentro de button
e vamos dizer a ele: Que tudo que estiver desabilitado em nossa aplicação [disabled] vamos colar um `opacity:0.6;` que ira deixa ele bem mais clarinho e vamos colocar um `cursor: not-allowed;` que e plaquinha de não permitido.

<h1 align="center">
    <img src="./img/img018.png" />
</h1>

Agora vamos colocar as variavel de cor dentro do `root`

<h1 align="center">
    <img src="./img/img019.png" />
</h1>

### Fontes do Google Fonts

Vamos configura uma fonte diferente na aplicação.
E maioria das fontes que os Web design vão ultizar esta disponiveis site do google font:

https://fonts.google.com/
Mais vamos em:
https://fonts.google.com/specimen/Poppins

E vamos selecionar os tamanho que vamos usa na aplicação:
400 regular
600 semi-bold

via link:

E vamos colocar dentro do `index.html`, deixando o `preconnect` em cima, ficando assim:

<h1 align="center">
    <img src="./img/img020.png" />
</h1>

Agora no arquivo global do css, vamos defenir a fonte poppins, no corpo da aplicação, no imput, no textarea e no button:

```
body, input, textarea, button {
    font-family: 'Poppins', sans-serif;
    font-weight: 400;
  }
  h1, h2, h3, h4, h5, h6, strong {
    font-weight: 600;
  } 
```

<h1 align="center">
    <img src="./img/img021.png" />
</h1>
