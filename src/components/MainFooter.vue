<script setup>
import HomeView from '@/views/HomeView.vue'
import BuscarView from '@/views/BuscarView.vue'
import ContatoView from '@/views/ContatoView.vue'

import { ref, computed } from 'vue'

const email = ref('')
let enviar = ref(false)

function confirmacao() {
    console.log(enviar)
    email.value = ""
    return true;
}

</script>
<template>
    <div class="main-footer">
        <div class="contato">
            <h1>CONTATO</h1>

            <div class="contact-form">
                <form @submit.prevent="enviar = confirmacao()">
                    <div class="info">

                        <div>
                            <p>
                                <img class="img1" src="@/assets/imgs/localizacao.png" alt="">
                                Av Do Principe, 1186, Itapema do Norte - Itapoá /SC
                            </p>
                        </div>
                        <div>
                            <p>
                                <img class="img1" src="@/assets/imgs/mensagem.png" alt="">
                                rfconsultoriaimobiliaria@outlook.com.br
                            </p>
                        </div>
                        <div>
                            <p>
                                <img class="img1" src="@/assets/imgs/telefone.png" alt="">
                                (47) 3443-3178
                            </p>
                        </div>
                        <div>
                            <p>
                                <img class="img1" src="@/assets/imgs/whatszapp.png" alt="">
                                (47) 99684-3087
                            </p>
                        </div>
                    </div>
                </form>
            </div>
        </div>

        <div class="links">
            <h1>LINKS</h1>
            <div>
                <p>
                    <router-link to="/" class="routerHome">Home</router-link>
                </p>
            </div>
            <div>
                <p>
                    <router-link to="/contato" class="routerFale">Fale conosco</router-link>
                </p>
            </div>
            <div>
                <p>
                    <router-link to="/buscar" class="routerBusca">Buscar imóveis</router-link>
                </p>
            </div>

        </div>
        <div class="entramos">
            <h1>ENTRAMOS EM CONTATO</h1>
            <form class="miniform" @submit.prevent="enviar = confirmacao()">
                <p>Ficou com dúvida de como alugar</p>
                <p>ou comprar o seu imóvel,</p>
                <p>entraremos em contato, digite o seu email</p>
                <input type="email" v-model="email" v-on:keypress="enviar = false" required placeholder="Email..." />
                <p class="pzin">Ao informar meus dados, eu</p>
                <p>concordo com a Política de Privacidade.</p>

                <button type="submit" class="comp">Enviar</button>
            </form>
        </div>
    </div>
</template>

<style scoped>
input {
    padding: 2%;
    width: 250px;
    font-size: medium;
    font-family: Arial, Helvetica, sans-serif;
    

}

.info {
    margin-left: 8%;
    margin-top: 180px;
    display: flex;
    flex-direction: column;
    font-size: 20px;
    padding: 0 0 0 70px;
    list-style: none;
    padding-left: 2px;
    position: relative;
    margin-bottom: 20px;
    line-height: 22px;
    color: #535353;
}

.img1 {
    margin-top: 5px;
    height: 28px;
    width: 25px;

}

.comp {
    color: white;
    height: 34px;
    width: 250px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 0%;
    border: 1px;
    font-size: 16px;
    background-color: #f28a31;
    margin-top: 20%;
    letter-spacing: 1px;
    justify-content: center;
    font-family: "Open Sans" sans-serif;
}

.routerBusca {
    text-decoration: none;
    color: #AAAAAA;
}

.routerHome {
    text-decoration: none;
    color: #AAAAAA;
}

.routerFale {
    text-decoration: none;
    color: #AAAAAA;
}

.pzin {
    margin-top: 15px;
}

.main-footer {
    padding: 10px 10px 500px 100px;
    background-color: #02193c;
    display: flex;
    flex-direction: row;
}

.contato {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding-left: 250px;
}

.entramos {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding-left: 250px;
}

.miniform {
    background-color: #021830;
    width: 280px;
    height: 350px;
    padding: 15px;
}

.links {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding: 0px, 10px, 20px, 60px;
    padding-left: 6%;
}


.main-footer div {
    color: #AAAAAA;
    margin: 0 15px 0 0;
    font-size: 12px;
}


h1 {
    font-size: medium;
    color: white;
    margin-top: 80px;
    margin-bottom: 30px;
}

@media (max-width: 768px) {
    input {
    padding: 2%;
    width: 250px;
    font-size: medium;
    font-family: Arial, Helvetica, sans-serif;
    

}

.info {
    margin-left: 8%;
    margin-top: 18px;
    display: flex;
    flex-direction: column;
    font-size: 20px;
    padding: 0 0 0 70px;
    list-style: none;
    padding-left: 2px;
    position: relative;
    margin-bottom: 20px;
    line-height: 22px;
    color: #535353;
}

.img1 {
    margin-top: 5px;
    height: 28px;
    width: 25px;

}

.comp {
    color: white;
    height: 34px;
    width: 250px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 0%;
    border: 1px;
    font-size: 16px;
    background-color: #f28a31;
    margin-top: 20%;
    letter-spacing: 1px;
    justify-content: center;
    font-family: "Open Sans" sans-serif;
}

.routerBusca {
    text-decoration: none;
    color: #AAAAAA;
}

.routerHome {
    text-decoration: none;
    color: #AAAAAA;
}

.routerFale {
    text-decoration: none;
    color: #AAAAAA;
}

.pzin {
    margin-top: 15px;
}

.main-footer {
        padding: 10px; /* Reduzi o padding para um valor único em todas as direções */
        background-color: #02193c;
        display: flex;
        flex-direction: column; /* Mudei a direção para "column" para empilhar os elementos verticalmente */
    }
.contato {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding-left: 250px;
}

.entramos {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding-left: 250px;
}

.miniform {
    background-color: #021830;
    width: 280px;
    height: 350px;
    padding: 15px;
}

.links {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding: 0px, 10px, 20px, 60px;
    padding-left: 6%;
}


.main-footer div {
    color: #AAAAAA;
    margin: 0 15px 0 0;
    font-size: 12px;
}


h1 {
    font-size: medium;
    color: white;
    margin-top: 80px;
    margin-bottom: 30px;

    }
    }

</style>
