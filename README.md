# Passoia
<p align="center">
    <img src="./src/assets/inspirePixel.gif" alt="Demonstração do Projeto" width="700"/>
</p>

## Informações do Curso 
- <b>Instituição:</b> Vai na Web

- <b>Curso:</b> Grupo BiT - L'oreal

- <b>Professores:</b> Kleber Matos, Carol Oliveira e Stéfany Farias

- <b>Autor(a):</b> Lucas Laino de Andrade

## Sobre o Projeto
> Status: Concluído ✅

O projeto é uma landing page de imagens similar ao pinterest, onde o usuário pode buscar inspiração através de fotos. Esse projeto é uma proposta para a resolução do desafio final do ciclo de front-end proposto pelo Grupo BiT da instituição Vai na Web, como o intuito de solidififcar o Vue.js e biblioteca Axios de forma terórica e prática.


## Tecnologias Utilizadas
Este projeto foi construído utilizando as seguintes tecnologias:

- Vue.js (para a componentização do site)

- Biblioteca Axios (para requisções para a API)

- API Loren Picsum (para busca de imagens utilizadas no projeto)

- CSS3 (para a estilização, layout com Flexbox e responsividade)

- SCSS (como pré-processador de CSS)

- Biblioteca Iconify (para ícones utilizados no cabeçalho e rodapé)

## Destaque
Gostaria de destacar o código que usei para fazer requisições a API e exibir as imagens na tela utilizando uma abordagem de função assíncrona e tratamento de erros: 
```
<script setup>
import Card from '../Card/Card.vue';
import axios from 'axios';
import { ref } from 'vue';

const imagens = ref([])

async function pegarImagem() {
    try {
        const resposta = await axios.get('https://picsum.photos/v2/list?page=2&limit=15');
        imagens.value = resposta.data;
    } catch (error) {
        console.log('Não foi possível carregar as imagens' + error);
    }
}
pegarImagem();
</script>

<template>
    <section class="galeria">
        <h2>Inspire-se</h2>

        <div class="imagens">
            <Card v-for="img in imagens" :imagem="img.download_url" />
        </div>
    </section>
</template>
```

## Como Executar o Projeto
Como o projeto é estático, não há necessidade de instalação de dependências ou servidores complexos.

Acesse pelo link [clicando aqui](https://inspirepixel.vercel.app/)

ou

1.Clone este repositório usando o comando: ```git clone https://github.com/LucasLaino/inspirePixel```

2.Navegue até a pasta do projeto.

3.Abra a pasta do projeto no editor de código (caso use Visual Studio Code, use a extensão Live Server).

4.Clique com o botão direito no arquivo index.html e selecione a opção "Open with Live Server" (ou utilize o atalho alt + L + O).

5.O site será aberto automaticamente no seu navegador no endereço http://127.0.0.1:5500.

## Contatos
- LinkedIn: [Lucas Laino](https://www.linkedin.com/in/lucaslaino) 
- E-mail: [lucaslaino00@gmail.com](mailto:lucaslaino00@gmail.com)