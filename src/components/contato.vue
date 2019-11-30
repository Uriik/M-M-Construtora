<template>
  <section id="fundo-importante" class="flex background-tudo column">
    <div class="flex flex1 contato ml0 mapa row">
      <div class="contatos flex1 p-horizontal-50">
        <div class="flex1">
          <h1 class="titulos ml0">contato</h1>
        </div>
        <ul class="flex column flex-start info-empresa">
          <li class="telefone englobando">
            <i class="fas fa-phone-square-alt informacoes-footer"></i>telefone 00000-0000
          </li>
          <li class="facebook englobando">
            <i class="fab fa-facebook informacoes-footer"></i>@m&mconstrutora
          </li>
          <li class="instagram englobando">
            <i class="fab fa-instagram informacoes-footer"></i>memcontrutora.com.br
          </li>
          <li class="endereco">
            <i class="fas fa-map-marker-alt informacoes-footer"></i>rua dos bobos travessa com eu não sei
          </li>
        </ul>
        <div class="maps">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3643.9515313536203!2d-46.51956678555738!3d-24.03277428445093!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce21d7c774d3ab%3A0xa666d0dd68829558!2sAv.%20Hermenegildo%20Pereira%20de%20Fran%C3%A7a%2C%20238%20-%20Balne%C3%A1rio%20Esmeralda%2C%20Praia%20Grande%20-%20SP%2C%2011713-290!5e0!3m2!1spt-BR!2sbr!4v1573407975235!5m2!1spt-BR!2sbr"
            width="100%"
            height="350"
            frameborder="0"
            style="border:0;"
            allowfullscreen
          ></iframe>
        </div>
      </div>

      <div class="flex2 bgform flex justify-content-center center">
        <!-- <div class="bobao">
          <p class="motivador">
            Manda uma mensagem pra gente!
            <br />Sua opinião é muito importante para nossa empresa.
          </p>
        </div>-->
        <div class="flex flex0 formulario column">
          <form class="formulario-contato flex column" >
            <label class="label-input">
              <p>
                Nome
                <span
                  class="error"
                  v-if="!$v.nome.required && $v.nome.$dirty"
                >*Este campo é obrigatório!</span>
                <span
                  class="error"
                  v-if="!$v.nome.minLength"
                >O nome dever ter pelo menos {{$v.nome.$params.minLength.min}} letters.</span>
              </p>
              <input
                type="text"
                class="input-default"
                v-model="$v.nome.$model"
                name="nome"
                required="required"
              />
            </label>

            <label class="label-input">
              <p>
                Email
                <span
                  class="error"
                  v-if="!$v.email.required && $v.email.$dirty"
                >*Este campo é obrigatório!</span>
                <span
                  class="error"
                  v-if="!$v.email.email && $v.email.$dirty"
                >*Este e-mail não é valido!</span>
                <span
                  class="error"
                  v-if="!$v.email.minLength"
                >O nome dever ter pelo menos {{$v.email.$params.minLength.min}} letters.</span>
              </p>
              <input
                type="email"
                class="input-default"
                v-model="$v.email.$model"
                name="email"
                required="required"
              />
            </label>

            <label class="label-input">
              <p>
                Assunto
                <span
                  class="error"
                  v-if="!$v.assunto.required && $v.assunto.$dirty"
                >*Este campo é obrigatório!</span>
                <span
                  class="error"
                  v-if="!$v.assunto.minLength"
                >O nome dever ter pelo menos {{$v.assunto.$params.minLength.min}} letters.</span>
              </p>
              <input
                type="text"
                class="input-default"
                v-model="$v.assunto.$model"
                name="assunto"
                required="required"
              />
            </label>

            <label class="label-input">
              <p>
                Mensagem
                <span
                  class="error"
                  v-if="!$v.mensagem.required && $v.mensagem.$dirty"
                >*Este campo é obrigatório!</span>
                <span
                  class="error"
                  v-if="!$v.mensagem.minLength"
                >O nome dever ter pelo menos {{$v.mensagem.$params.minLength.min}}</span>
              </p>
              <textarea
                v-model="$v.mensagem.$model"
                name="mensagem"
                class="input-default textarea-default"
                cols="30"
                rows="10"
              ></textarea>
              <p class="typo__p" v-if="submitStatus === 'OK'">Obrigado pela Mensagem!</p>
              <p class="typo__p" v-if="submitStatus === 'ERROR'">Preencha o formulário corretamente</p>
              <p class="typo__p" v-if="submitStatus === 'PENDING'">Aguarde...</p>
            </label>
            <label class="label-default flex align-self">
              <button
                @click="sendEmail()"
                name="enviar"
                class="btn-default"
                :disabled="submitStatus === 'PENDING'"
              >Enviar</button>
            </label>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script src= "https://smtpjs.com/v3/smtp.js"> </script>
<script>
import { required, email, minLength } from "vuelidate/lib/validators";
export default {
  data() {
    return {
      nome: "",
      email: "",
      assunto: "",
      mensagem: "",
      submitStatus: ""
    };
  },
  validations: {
    nome: {
      required,
      minLength: minLength(3)
    },
    email: {
      required,
      email,
      minLength: minLength(3)
    },
    assunto: {
      required,
      minLength: minLength(3)
    },
    mensagem: {
      required,
      minLength: minLength(10)
    }
  },
  
};

function sendEmail() {
      Email.send({
        Host: "smtp.elasticemail.com",
        Username: "veronicaribeirodesigner@gmail.com",
        Password: "9aa49fdf-348b-48fc-add9-2d573712a33b",
        To: this.email,
        From: "veronicaribeirodesigner@gmail.com",
        port:2525,
        Subject: this.assunto,
        Body: this.mensagem,
        TLS: Required
      }).then(message => alert("mail sent successfully"));
    }
</script>


<style>
.contato {
  margin-left: 50px;
}
.info-empresa {
  margin-bottom: 20px;
}
ul {
  margin: 0px;
  padding: 0px;
}
ul > li {
  list-style-type: none;
}
.icon-contato {
  font-size: 1rem;
  color: #f7f;
}
.informacoes-footer {
  margin-right: 10px;
}

.englobando {
  margin-bottom: 10px;
}

#fundo-importante {
  /* background-color: #f7f7f7; */
  /* background-image: linear-gradient(to left, #f7f7f7 60%, #fff 40%); */
}
.bgform {
  background-color: #f7f7f7;
}
.bobao {
  justify-content: center;
}
.motivador {
  text-align: start;
}
.formulario {
  /* margin: 0 50vh; */
  text-align: start;
}

.error {
  color: red;
}
.typo__p {
  color: red;
  font-size: 0.7rem;
}

p {
  margin: 0;
}
</style>

