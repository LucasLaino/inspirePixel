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
    align-items: center;
    justify-content: space-around;

    .inspiraPixel-infos {
        h1 {
            font-size: 40px;
            width: 400px;

            span {
                font-size: 50px;
                color: #E1306C;
            }
        }

        p {
            font-size: 20px;
            width: 650px;
        }
    }

    img {
        width: 25vw;
    }
}

@media (min-width: 350px) and (max-width: 480px) {
    .hero {
        flex-direction: column-reverse;
        justify-content: center;
        gap: 20px;

        .inspiraPixel-infos {
            text-align: center;
            
            h1 {
                font-size: 30px;
                width: 100vw;

                span {
                    font-size: 35px;
                }
            }

            p {
                width: 100vw;
                padding: 30px 0;
            }
        }

        img {
            width: 80vw;
            padding-top: 30px;
        }
    }
}
</style>