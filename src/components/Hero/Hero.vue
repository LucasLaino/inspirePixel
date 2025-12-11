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
    padding: 30px 0;

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
        }
    }
}

@media (min-width: 481px) and (max-width: 768px) {
    .hero {
        .inspiraPixel-infos {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            width: 50vw;

            h1 {
                font-size: 25px;

                span {
                    font-size: 35px;
                }
            }

            p {
                width: 350px;
                font-size: 16px;
            }
        }

        img {
            width: 40vw;
        }
    }
}
</style>