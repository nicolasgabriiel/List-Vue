### To-Do List Vue 

## Sumário

- [Resumo](#Resumo)
  - [Desafio](#Desafio)
  - [Screenshot](#screenshot)
  - [Link](#link)
- [Processo](#Processo)
  - [Construido com](#construido-com)
  - [O que eu aprendi](#o-que-eu-aprendi)
- [Autor](#autor)

## Resumo

O desafio foi construir uma To-Do List utilizando Vue.js, TypeScript e Tailwind.


### Desafio

Foi a minha primeira vez desenvolvendo uma To-Do List, foi uma experiência pra lá de desafiadora. Meu objetivo era entender mais sobre o vue.js e suas funções, sintáxe e métodos próprios, criar interfaces com o typescript e utilizar pela primeira vez o framework css Tailwind para estilizar o projeto. 



### Screenshots

<p align="center"> Home</p>
  <div align="center"><img width="600px" src="./src/assets/gif.gif"></img> </div>




### Link: https://card-compenent.vercel.app

## Processo

### Construido com

-Vue.JS <br>
-TypeScript <br>
-HTML5 <br>
-CSS3 <br>
-JavaScript <br>

### Principais coisas que aprendi

Enviar dados para um componente filho

```js
   <CardConcluido :valor-esperado='valor' />
```

Receber dados de um elemento pai através de propriedades

```js
    props: {
        valorEsperado: {
            type: Number,
            default: 0,
        }
```

Criar dados que funcionam como variáveis

```js
  data(){
    return{
      hide: false,
      valor: 0
    }
```

Utilizando métodos
```js
methods:{
    Funcao(){
      this.hide = true
    }
```
Enviando dados para o componente pai com o Emit
```js
this.$emit('hide')
```

Recebendo dados emitidos do componente filho
```js
     <Card v-on:hide="Funcao"/>
```

Passando um dado dentro de um emmit 
```js
 this.$emit('valor', { meuValor: this.escolhido } )
```


## Autor

-  Site pessoal - [Nicolas Gabriel](https://www.linkedin.com/in/nicolasgabriiel/)

<div  align="left">


