<script setup>
import { ref, computed } from 'vue'


const nome = ref('')
const email = ref('')
const celular = ref('')
const telefone = ref('')
const mensagem = ref('')
let enviar = ref(false)

function confirmacao() {
    console.log(enviar)
    nome.value = "";
    email.value = "";
    celular.value = "";
    telefone.value = "";
    mensagem.value = ""
    return true;
}

</script>
<template>
    <div class="row">
        <div class="banner">
            <div class="inner-text">
                <h1 class="titu">CONTATO</h1>
            </div>
        </div>
        <div class="titu2">
            <h1 class="CO">
                CONTATO
            </h1>
            <h4>Escolha um dos canais para que possamos responder o mais rápido possível.</h4>
        </div>


        <div class="contact-form">
            <form @submit.prevent="enviar = confirmacao()">
                <div class="info">
                    <h3 class="titu3">Informações de contato </h3>
                    <div>
                        <img class="img1" src="@/assets/imgs/loc.png" alt="">
                        Av Do Principe, 1186, Itapema do Norte - Itapoá /SC
                    </div>
                    <div>
                        <img class="img1" src="@/assets/imgs/caixa.png" alt="">
                        rfconsultoriaimobiliaria@outlook.com.br
                    </div>
                    <div>
                        <img class="img1" src="@/assets/imgs/telefone2.png" alt="">
                        (47) 3443-3178
                    </div>
                    <div>
                        <img class="img1" src="@/assets/imgs/wpp.png" alt="">
                        (47) 99684-3087
                    </div>
                </div>

                <!-- contato-formulario -->
                <div class="container-form">
                    <form class="form" @submit.prevent="enviar = confirmacao()">
                        <div class="centro">
                            <div class="dados">
                                <br>
                                <div class="nome">
                                    <input type="text" v-model="nome" v-on:keypress="enviar = false" required
                                        placeholder="Digite seu nome" />
                                </div>

                                <div class="email">
                                    <input type="email" v-model="email" v-on:keypress="enviar = false" required
                                        placeholder="Digite seu email" />
                                </div>
                                <br>
                                <div class="telefoneCL">
                                    <input type="telefoneCL" v-model="celular" v-on:keypress="enviar = false" minlength=""
                                        required placeholder="Digite seu celular" />
                                </div>

                            
                                <div class="telefoneFX">
                                    <input type="telefoneFX" v-model="telefone" v-on:keypress="enviar = false" minlength=""
                                        required placeholder="Digite seu telefone" />
                                    <p></p>
                                </div>

                                <div class="mensagem">
                                    <textarea class="textarea-balao-up" v-model="mensagem" v-on:keypress="enviar = false" 
                                    required placeholder="Mensagem">
                                    </textarea>
                                </div>
                                <br>
                                <br>
                                <br>
                                <button type="submit" class="comp">Enviar</button>

                            </div>
                        </div>
                    </form>

                </div>
            </form>
        </div>
    </div>
        <div v-if="enviar" class="baixo">
            <p> SUA MENSAGEM FOI ENVIADA, AGUARDE SEU RETORNO!</p>
        </div>

</template>

<style scoped>
.centro {
    margin-top: -18%;
}

.form {
    height: 650px;
    max-width: 700px;
    padding: 25px;
    /* border: 1px solid #ccc; */
    /* background-color: #848486; */
    width: 85vh;
    font-family: "Open Sans" sans-serif;
    transform: scale(0.8);
    font-size: 22px;
    margin-top: 4%;
}


.info {
    margin-left: 8%;
    margin-top: 50px;
    display: flex;
    flex-direction: column;
    font-size: 14px;
    padding: 0 0 0 70px;
    list-style: none;
    padding-left: 40px;
    position: relative;
    margin-bottom: 20px;
    line-height: 22px;
    color: #535353;
}

textarea {
    resize: none;
    width: 1000px;
    height: 400px;

}

.baixo {
    margin-left: 15%;
    margin-top: -5%;
    flex-direction: row;
    font-size: medium;
    font-family: "Open Sans" sans-serif;
    justify-content: center;
    border: 5px;
    display: flex;
     font-weight: bold;

}

.comp {
    color: white;
    height: 40px;
    width: 90px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 47%;
    border: 1px;
    font-size: 21px;
    background-color: #f28a31;
    margin-top: 20%;
}

.nome {
    display: flex;
    flex-direction: column;
    align-items: baseline;
    margin-top: 8%;
    /* margin-bottom: 10%; */
}

.email {
    margin-right: -8%;
    margin-top: -6%;
    display: flex;
    flex-direction: column;
    align-items: end;
}

.telefoneCL {
    margin-top: -3%;
    display: flex;
    flex-direction: column;
    align-items: baseline;
    /* margin-bottom: 20%; */
}


.telefoneFX {
    margin-right: -8%;
    margin-top: -6%;
    display: flex;
    flex-direction: column;
    align-items: end;
}

.mensagem {
    width: 650px;
    height: 200px;
    display: flex;
    /* align-items: end; */
}

h2 {
    font-size: 25px;
}

.container-form {
    margin-left: 35%;
    margin-top: -19%;
}

.row {
    
    margin-right: -15px;
    margin-left: -15px;
}

.titu {
    color: white;
}

.titu2 {
    display: flex;
    flex-direction: column;
    align-items: center;

}

.titu3 {
    padding: 0 0 0 20px;
}
.dados {
    font-family: Arial, Helvetica, sans-serif;
    /* color: black; */
}

.img1 {
    height: 38px;
    width: 45px;
}

.banner {
    border-radius: 0%;
    background: url(https://www.rafaelfonsecaimoveis.com.br/assets/img/anuncie/banner-anuncie.png) top left repeat;
    background-repeat: no-repeat;
    background-size: cover;
    background-size: cover;
    height: 280px;
    background-position: center center;
    background-repeat: no-repeat;
    position: relative;
    background-color: rgba(36, 42, 53, 0.7);
    /* color: aliceblue; */
    display: flex;
    align-items: center;
    flex-direction: column;
    /* padding: 100px 0 0 0 ; */
}

.inner-text {
    height: 100%;
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    background-color: black;
    opacity: 70%;
}

.CO {
    font-size: 25px;
    margin-top: 30px;
    color: #37404D;
}

@media (max-width: 768px) {
    .centro {
        margin-top: -18%;
    }

    .form {
        height: 650px;
        max-width: 700px;
        padding: 25px;
        width: 85vh;
        font-family: "Open Sans", sans-serif;
        font-size: 22px;
        margin-top: 4%;
    }

    .info {
        margin-left: 1%;
        margin-top: 45px;
        display: flex;
        flex-direction: column;
        font-size: 14px;
        padding: 0 0 0 70px;
        list-style: none;
        padding-left: 60px;
        position: relative;
        margin-bottom: 20px;
        line-height: 22px;
        color: #535353;
    }

    textarea {
        resize: none;
        width: 1000px;
        height: 400px;
    }
    .email {
    margin-right: 0%;
    margin-top: -6%;
    display: flex;
    flex-direction: column;
    align-items: end;
}

.telefoneCL {
    margin-top: -3%;
    display: flex;
    flex-direction: column;
    align-items: baseline;
    /* margin-bottom: 20%; */
}

.telefoneFX {
    margin-right: 0%;
    margin-top: -6%;
    display: flex;
    flex-direction: column;
    align-items: end;
}

.mensagem {
    width: 650px;
    height: 200px;
    display: flex;
    /* align-items: end; */
}

    .baixo {
        margin-left: 5%;
        margin-top: -5%;
        flex-direction: row;
        font-size: medium;
        font-family: "Open Sans", sans-serif;
        justify-content: center;
        border: 1px solid; /* Adicionei o estilo de borda */
        display: flex;
        font-weight: bold;
    }

    .comp {
        color: white;
        height: 40px;
        width: 90px;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-left: 5%; 
        border: 1px solid; 
        font-size: 21px;
        background-color: #f28a31;
        margin-top: 20px; 
    }

    .container-form {
        margin-left: 5%; 
        margin-top: -5%; 
    }

    .row {
        margin-right: 0;
        margin-left: 0;
    }

    .titu {
        color: white;
    }

    .titu2 {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .titu3 {
        padding: 0 0 0 20px;
    }

    .dados {
        font-family: Arial, Helvetica, sans-serif;
    }

    .img1 {
        height: 50px;
        width: 50px;
    }

    .banner {
        border-radius: 0;
        background: url(https://www.rafaelfonsecaimoveis.com.br/assets/img/anuncie/banner-anuncie.png) top left repeat;
        background-repeat: no-repeat;
        background-size: cover;
        height: 280px;
        background-position: center center;
        background-repeat: no-repeat;
        position: relative;
        background-color: rgba(36, 42, 53, 0.7);
        display: flex;
        align-items: center;
        flex-direction: column;
    }

    .inner-text {
        height: 100%;
        width: 100%;
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        background-color: black;
        opacity: 0.7; /* Corrigi o valor de opacidade */
    }

    .CO {
        font-size: 25px;
        margin-top: 30px;
        color: #37404D;
    }
}

@media (max-width: 480px) {
    /* Estilos para telas ainda menores, como smartphones */
    /* Faça alterações mais significativas no layout, como tornar os elementos em bloco */
}
</style>