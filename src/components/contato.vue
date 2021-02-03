<template>
  <section id="fundo-importante" class="flex background-tudo column">
    <div class="flex flex1 contato ml0 mapa row">
      <div class="contatos flex1 p-horizontal-50">
        <div class="flex1">
          <h1 class="titulos ml0">contato</h1>
        </div>
        <ul class="flex column flex-start info-empresa">
          <li class="telefone englobando">
            <i class="fas fa-phone-square-alt informacoes-footer"></i>telefone (13) 97414-2011
          </li>
          <li>
            <address>
              <i class="fas fa-envelope-open"></i>
              <a
                href="mailto:mmconstrucao013@gmail.com"
                class="email-color"
              >mmconstrucoes869@gmail.com</a>
            </address>
          </li>
          <li class="facebook englobando">
            <i class="fab fa-facebook informacoes-footer"></i>@m&mconstrutora
          </li>
          <li class="instagram englobando">
            <i class="fab fa-instagram informacoes-footer"></i>memconstrutora.com.br
          </li>
          <li class="endereco">
            <i class="fas fa-map-marker-alt informacoes-footer"></i>Rua Doutor Ernesto Vergara n°971
          </li>
        </ul>
        <div class="maps">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3644.292510267259!2d-46.474469485557805!3d-24.02074808445673!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce1ef945a2866f%3A0xbd0d6e315ac083fa!2sR.%20Dr.%20Ernesto%20Vergara%2C%20971%20-%20Vila%20Assuncao%2C%20Praia%20Grande%20-%20SP%2C%2011704-080!5e0!3m2!1spt-BR!2sbr!4v1578707180961!5m2!1spt-BR!2sbr"
            width="100%"
            height="350"
            frameborder="0"
            style="border:0;"
            allowfullscreen
          ></iframe>
        </div>
      </div>

      <div class="flex2 bgform flex justify-content-center center">
        
        <div class="flex flex0 formulario column">
          <form class="formulario-contato flex column">
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
                Telefone
                <span
                  class="error"
                  v-if="!$v.telefone.required && $v.telefone.$dirty"
                >*Este campo é obrigatório!</span>
                <span
                  class="error"
                  v-if="!$v.telefone.minLength"
                >O telefone dever ter pelo menos {{$v.telefone.$params.minLength.min}} letters.</span>
              </p>
              <input
                type="text"
                class="input-default"
                v-model="$v.telefone.$model"
                name="telefone"
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

<script src= "https://smtpjs.com/v3/smtp.js">
</script>
<script>
import { required, email, minLength } from "vuelidate/lib/validators";
export default {
  data() {
    return {
      nome: "",
      telefone: "",
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
    telefone: {
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
  }
};

function sendEmail() {
  Email.send({
    Host: "smtp.elasticemail.com",
    Username: "veronicaribeirodesigner@gmail.com",
    Password: "9aa49fdf-348b-48fc-add9-2d573712a33b",
    To: this.email,
    From: "veronicaribeirodesigner@gmail.com",
    port: 2525,
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
a.email-color {
  color: #e84c3d;
  margin-left: 5px;
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
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  section#fundo-importante {
    background-color: #f7f7f7;
    height: 100%;
    padding-bottom: 15px;
  }
  #fundo-importante .row {
    flex-direction: column;
  }
  #fundo-importante.background-tudo > .contato.m10.row {
    margin-left: 15px;
  }
  #fundo-importante {
    flex-direction: column;
  }
  .contatos {
    flex-direction: column;
  }
  .contatos.p-horizontal-50 {
    padding: 0 15px;
  }
  section#fundo-importante .bgform {
    display: none;
  }
}
</style>

