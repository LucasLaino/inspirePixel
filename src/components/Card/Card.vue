<script setup>
import { Icon } from '@iconify/vue';
defineProps(['imagem'])
</script>

<template>
    <div class="card">
        <button>
            <Icon icon="basil:heart-solid" width="30" height="30" style="color: #fff" />
        </button>
        <img :src="imagem" alt="Praia do Arpoador">
    </div>
</template>

<style scoped lang="scss">
.card {
    width: 300px;
    height: 400px;
    position: relative;
    margin: 0 5px;

    button {
        position: absolute;
        right: 8px;
        top: 5px;
        border: none;
        background-color: transparent;
    }

    img {
        border-radius: 10px;
        width: 100%;
        height: 100%;
    }
}
</style>