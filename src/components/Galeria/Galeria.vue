<script setup>
import Card from '../Card/Card.vue';

</script>

<template>
    <section class="galeria">
        <h2>Inspire-se</h2>

        <div class="imagens">
            <Card imagem="https://picsum.photos/300/500" />
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
        justify-content: space-evenly;
        flex-wrap: wrap;
        gap: 20px;
    }
}
</style>