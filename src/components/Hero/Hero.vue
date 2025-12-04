<script setup></script>

<template>
    <section class="hero">
        <article class="inspiraPixel-infos">
            <h1>Onde a Paisagem Vira <span>Inspiração</span>.</h1>
            <p>Explore paisagens, cores e luzes que inspiram novas histórias através da fotografia.</p>
        </article>

        <img src="../../assets/fotografo.jpg" alt="Imagem Fotografo">
    </section>
</template>

<style scoped>
.hero {
    display: flex;
    margin: 50px 0;
    align-items: center;
    justify-content: space-evenly;

    h1 {
        width: 400px;
        font-size: 40px;

        span {
            font-size: 50px;
            color: #E1306C;
        }
    }

    p {
        width: 680px;
        font-size: 20px;
    }

    img {
        width: 25%;
    }
}
</style>