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
    transition: 0.3s ease-in-out;

    &:hover {
        transform: scale(1.1);
        cursor: pointer;
    }

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

@media (min-width: 481px) and (max-width: 768px) {
    .card {
        width: 250px;
        height: 350px;
    }
}
</style>