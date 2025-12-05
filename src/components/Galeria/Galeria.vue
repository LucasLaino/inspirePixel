<script setup>
import Card from '../Card/Card.vue';
import axios from 'axios';
import { ref } from 'vue';

const imagens = ref([])

async function pegarImagem() {
    try {
        const resposta = await axios.get('https://picsum.photos/v2/list?page=2&limit=15');
        imagens.value = resposta.data;
    } catch(error) {
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

<style scoped lang="scss">
.galeria {
    h2 {
        font-size: 30px;
        color: #262626;
        margin-left: 20px;
    }

    .imagens {
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
        gap: 15px;
    }
}
</style>