<script setup>
import { Icon } from '@iconify/vue';
</script>

<template>
    <footer class="footer">
        <section class="contato">
            <h4>Contato</h4>
            <ul>
                <li>contato@inspiralens.com</li>
                <li>Central de Ajuda</li>
                <li>Rio de Janeiro - Brasil</li>
            </ul>
        </section>

        <section class="sobre">
            <h4>Sobre</h4>

            <ul>
                <li>Políticas</li>
                <li>Políticas de Privacidade</li>
                <li>Blog</li>
            </ul>
        </section>

        <section class="newsletter">
            <h4>Assine Nossa Newsletter</h4>

            <form class="form-newsletter">
                <input type="email" placeholder="seu e-mail">

                <button>Inscrever-se</button>
            </form>
        </section>
    </footer>

    <section class="redes-sociais">
        <Icon icon="logos:facebook" width="24" height="24" />
        <Icon icon="logos:linkedin-icon" width="24" height="24" />
        <Icon icon="logos:instagram-icon" width="24" height="24" />
        <Icon icon="logos:x" width="24" height="24" />
    </section>
</template>

<style scoped>
.footer {
    display: flex;
    justify-content: space-between;
    padding: 80px;

    .contato ul li,
    .sobre ul li {
        margin: 10px 0;
    }

    .form-newsletter {
        display: flex;
        flex-direction: column;
        gap: 20px;

        input {
            border: none;
            margin-top: 20px;
        }

        button {
            background-color: #E1306C;
            border: none;
            color: #FFF;
            padding: 5px;
            border-radius: 5px;
        }
    }
}

.redes-sociais {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-bottom: 50px;
}
</style>