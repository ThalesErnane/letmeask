Ferramentas utilizadas 

Node - utilizar JS fora do browser 
Yarn - gerenciador de pacotes
Firebase - banco de dados 


Assuntos abordados - Sobre 
SPA single page application 

Conceitos do React 

Componetes 
Exemplos: 

'./components/Button.tsx'

function Button() {
    return (

    )
}

Propriedade
Exemplo:

type ButtonProps = {
    text?: string;
    children: string;
}

export function Button(props: ButtonProps) {
    return (
        <button>{props.text || 'Default'}</button>
    )
}

// ------------------------------------------------- //

import { Button } from './components/Button'

function App() {
  return (
    <div>
      <Button text="Botão 1"/>
      <Button> Usando Children </Button>
      <Button />
      <Button />
    </div>
  );
}

Estado 

import {useState} from  "react";

export function Button() {
    (counter = 0, valor inicial)
    (setCounter = função)
    const [counter, setCounter] = useState(0) 
    function increment() {
        setCounter(counter + 1);
        console.log(counter);
    }
    return (
        <button onClick={increment}>{counter}</button>
    )
}


Criando o Projeto 
yarn create react-app letmeask --template typescript

React 
fast refresh 

HTML dentro do JS = JSX


RealTime DataBase

// utilizando webpack (Module Bundler)

instalando dependência do sass
yarn add node-sass@^5.0.0


Utilizando Spread Operator 

import { ButtonHTMLAttributes } from 'react';

type ButtonProps = ButtonHTMLAttributes<HTMLButtonElement>

export function Button(props: ButtonProps) {
    return (
        <button className="button" {...props}/>
    )
}

--------------------------------------------------------------
Trabalhando com roteamento de paginas com biblioteca router-dom

instalando o react-router-dom 
yarn add react-router-dom
yarn add @types/react-router-dom D

Utilizando Contextos no React

Exemplo: 

import { createContext } from 'react';

import { Home } from "./pages/Home";
import { NewRoom } from "./pages/NewRoom";

import { BrowserRouter, Route} from 'react-router-dom'

const TestContext = createContext('');

function App() {
  return (
  <BrowserRouter>
    <TestContext.Provider value={'Teste'}> 
      <Route path="/" exact component={Home} />
      <Route path="/rooms/new" component={NewRoom} />
    </TestContext.Provider>
  </BrowserRouter>
  );
}

export default App;
---------------------------------------------------------------

terminar 40min

{
  "rules": {
    "rooms": {
      ".read": false,
      ".write": "auth != null",
      "$roomId": {
        ".read": true,
        ".write": "auth != null && (!data.exists() || data.child('authorId').val() == auth.id)",
        "questions": {
          ".read": true,
          ".write": "auth != null && (!data.exists() || data.parent().child('authorId').val() == auth.id)",
          "likes": {
            ".read": true,
            ".write": "auth != null && (!data.exists() || data.child('authorId').val() == auth.id)",  
          }
        }
      }
    }
  }
}

terminar 30min

instalando yarn add classnames 

