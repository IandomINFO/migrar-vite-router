
Primeiramente você deve alterar a linha de comando do package.json do seu projeto de: 

    "dependencies": {
    "vue": "^3.2.33",
    },
  
  (ou algo similiar a isso) e adicionar a linha "vue-router": "^4.0.14", ficando assim:
  
    "dependencies": {
    "vue": "^3.2.33",
    "vue-router": "^4.0.14"
    },
  
  Após essa mudança você deve abrir o terminal e instalar o pacote com o comando "npm i".
  Feito isso você deve alterar a linha de código do seu main.js para:
  
    import { createApp } from "vue";
    import App from "./App.vue";
    import router from "./router";

    import "@/assets/base.css";

    const app = createApp(App);

    app.use(router);

    app.mount("#app");


(caso esteja usando outro nome de folha de estilo css apenas altere de "base.css" para o "nome-do-seu-arquivo.css")

  Feito isso você deve baixar ou recriar os arquivos que estão disponibilizados nesse repositório dentro do seu projeto, os arquivos são:
  
  A pasta router com o arquivo index.js dentro.
  A pasta views vazia (a pasta views é o lugar onde os seus componentes de pagina raiz irão ficar).
