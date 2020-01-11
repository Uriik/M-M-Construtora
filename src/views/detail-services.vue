<template>
  <section class="flex backgrounduni column">
    <div class="flex ">
      <div class="flex1">
        <div class="fotoVazamento">
          <span class="voltar flex" @click="voltar()"> Voltar</span><br />
          <img :src="servicos[this.param].img" alt />
        </div>
      </div>

      <div class="textoVazamentos flex1">
        <h1 class="tituloUnico">{{ servicos[this.param].title }}</h1>
        <p class="textoForm">
          {{ servicos[this.param].description }}
        </p>
      </div>
    </div>
    <section class="column flex backgroundNo cards-details">
      <div class="flex flex1 cards">
        <article @click="mudaConteudo(0)" class="card flex1">
          <article>
            <div class="contentImagem">
              <img
                class="img-responsive"
                src="@/assets/servicos/caca.jpg"
                alt
              />
            </div>
            <div class="contentDescription">
              <h3 class="subTitle">caça vazamentos</h3>
              <p>Lorem Ipsum</p>
            </div>
          </article>
        </article>
        <article @click="mudaConteudo(1)" class="card flex1">
          <article>
            <div class="contentImagem">
              <img
                class="img-responsive"
                src="@/assets/servicos/demolicao.jpg"
                alt
              />
            </div>
            <div class="contentDescription">
              <h3 class="subTitle">reformas em geral</h3>
              <p>Lorem Ipsum</p>
            </div>
          </article>
        </article>
        <article @click="mudaConteudo(2)" class="card flex1">
          <div>
            <div class="contentImagem">
              <img
                class="img-responsive"
                src="@/assets/servicos/pintura.jpg"
                alt
              />
            </div>
            <div class="contentDescription">
              <h3 class="subTitle">pintura</h3>
              <p>Lorem Ipsum</p>
            </div>
          </div>
        </article>
        <article @click="mudaConteudo(3)" class="card flex1">
          <article>
            <div class="contentImagem">
              <img
                class="img-responsive"
                src="@/assets/servicos/reformas.jpg"
                alt
              />
            </div>
            <div class="contentDescription">
              <h3 class="subTitle">contrução civil</h3>
              <p>Lorem Ipsum</p>
            </div>
          </article>
        </article>
      </div>
    </section>
    <footer class="rodape flex containaer-rodape space-between center">
    <div class="copyright">
      <p>Copyright todos os direitos reservados - 2019</p>
    </div>
    <div class="dev">
      <p>
        Desenvolvido por:
        <br />
        <span class="meu-nome">Gabriel</span>
      </p>
    </div>
  </footer>
  </section>
</template>
<script>
// import nosos from "@/components/nosos.vue";

export default {
  name: "Servicos",
  data() {
    return {
      param: this.$route.params.id,
      servicos: [
        {
          cd: 0,
          title: "caça vazamentos",
          img: require("@/assets/servicos/caca.jpg"),
          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin"
        },
        {
          cd: 1,
          title: "Reformas em Geral",
          img: require("@/assets/servicos/demolicao.jpg"),

          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin"
        },
        {
          cd: 2,
          title: "Pintura",
          img: require("@/assets/servicos/pintura.jpg"),

          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin"
        },
        {
          cd: 3,
          title: "Construção Civil",
          img: require("@/assets/servicos/reformas.jpg"),

          description:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has        survived not only five centuries, but also the leap into electronic typesettin"
        }
      ]
    };
  },
  methods: {
    mudaConteudo(cdConteudo) {
      this.param = cdConteudo;
    },
    voltar() {
      window.history.length > 1 ? this.$router.go(-1) : this.$router.push("/");
    }
  }
};
</script>
<style>
section.cards-details {
  /* height: 50vh; */
}

.backgrounduni {
  background-image: url("../assets/grupo25.svg");
  background-repeat: no-repeat;
  background-position: left;
  background-size: contain;
  justify-content: space-between;
}

.textoVazamentos {
  flex-direction: column;
  right: 100vh;
  margin-top: 7vh;
}
.textoForm {
  margin-right: 20px;
  text-align: left;
  text-align: justify;
  margin-top: 50px;
  margin-bottom: 0;
}
.fotoVazamento {
  margin-top: 6vh;
  margin-left: 15vh;
  max-width: 100vw;
}

.tituloUnico {
  color: rgb(232, 76, 61);
  font-weight: 800;
  font-size: 2rem;
  text-align: start;
  text-transform: uppercase;
}

.cards {
  margin: 0 50px;
  align-items: center;
  align-items: flex-end;
  margin-bottom: 10vh;

}
.cards article {
  cursor: pointer;
}
a.card {
  text-decoration: none;
}
.card {
  margin-right: 1vw;
}
.card:last-child {
  margin-right: 0;
}
.subTitle {
  text-transform: uppercase;
  margin: 0;
  padding: 0;
}

.contentDescription {
  background: rgb(4, 85, 125);
  color: rgb(255, 255, 255);
  padding: 15px 5px;
}

.contentDescription p {
  margin: 0;
  padding: 0;
}

.contentImagem {
  margin-bottom: -6px;
}
.voltar {
  cursor: pointer;
  color: #fff;
}


footer {
  height: 15vh;
  background: rgb(14, 29, 46);
  padding: 0 50px;
}

.rodape {
  color: white;
}

.text-rodape {
  height: 100%;
}

.dev{
    text-align:right;
}

.meu-nome{
    font-weight: bold;
}
</style>
