<script setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue';

const menuAtivo = ref(false);

function menuResponsivo() {
    menuAtivo.value = !menuAtivo.value;
}

</script>

<template>
    <header class="header">
        <img src="../../assets/logo-inspirePixel.svg" alt="Logo InspirePixel">

        <nav>
            <div class="mobile-menu" :class="{ 'active': menuAtivo }" @click="menuResponsivo">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
            
            <ul class="header-menu" :class="{ 'active': menuAtivo }">
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
    margin: 0 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 8vh;

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

    .mobile-menu {
        display: none;
        cursor: pointer;

        div {
            width: 32px;
            height: 2px;
            background-color: #E1306C;
            margin: 8px;
        }
    }
}

@media (max-width: 768px) {
    .header {
        .mobile-menu {
            display: block;
        }

        .header-menu {
            position: absolute;
            top: 8vh;
            right: 0;
            width: 40vw;
            height: 30vh;
            background-color: #FFF;
            flex-direction: column;
            align-items: center;
            transform: translateX(100%);
            transition: transform 0.3s ease-in;

            &.active {
                transform: translateX(0);
            }
        }
    }

    .mobile-menu.active .line1 {
        transform: rotate(-45deg) translate(-8px, 8px);
        transition: transform 0.3s ease-out;
    }

    .mobile-menu.active .line2 {
        opacity: 0;
        transition: transform 0.3s ease-in-out;

    }

    .mobile-menu.mobile-menu.active .line3 {
        transform: rotate(45deg) translate(-5px, -7px);
        transition: transform 0.3s ease-in-out;

    }
}
</style>
