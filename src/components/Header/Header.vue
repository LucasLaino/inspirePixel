<script setup>
import { Icon } from '@iconify/vue';
</script>

<template>
    <header class="header">
        <img src="../../assets/logo-inspirePixel.svg" alt="Logo InspirePixel">

        <nav>
            <ul class="header-menu">
                <li>
                    <a href="">
                        <Icon icon="material-symbols:search" width="24" height="24" />
                    </a>
                </li>
                <li><a href="">Início</a></li>
                <li><a href="">Galeria</a></li>
                <li><a href="">Favoritos</a></li>
                <li>
                    <a href="">
                        <Icon icon="material-symbols:person" width="24" height="24" />
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

.header {
    margin: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;

    img {
        width: 40px;
    }

    .header-menu {
        gap: 20px;
        display: flex;
        align-items: center;
        justify-content: center;

        li a {
            color: #262626;
        }
    }
}
</style>
