<template>
  <section class="column flex backgroundNo" id="nossosServicos">
    <div class="flex0">
      <h1 class="tituloNo">nossos serviços</h1>
    </div>
    <div class="flex flex1 cards">
      <router-link to="/detalhes/0" class="card flex1">
        <article>
          <div class="contentImagem">
            <img class="img-responsive" src="@/assets/servicos/caca.jpg" alt />
          </div>
          <div class="contentDescription">
            <h3 class="subTitle">caça vazamentos</h3>
            <p></p>
          </div>
        </article>
      </router-link>
      <router-link to="/detalhes/1" class="card flex1">
        <article>
          <div class="contentImagem">
            <img class="img-responsive" src="@/assets/servicos/demolicao.jpg" alt />
          </div>
          <div class="contentDescription">
            <h3 class="subTitle">reformas em geral</h3>
            <p></p>
          </div>
        </article>
      </router-link>
      <router-link to="/detalhes/2" class="card flex1">
        <div>
          <div class="contentImagem">
            <img class="img-responsive" src="@/assets/servicos/pintura.jpg" alt />
          </div>
          <div class="contentDescription">
            <h3 class="subTitle">pinturas e texturas</h3>
            <p></p>
          </div>
        </div>
      </router-link>
      <router-link to="/detalhes/3" class="card flex1">
        <article>
          <div class="contentImagem">
            <img class="img-responsive" src="@/assets/servicos/reformas.jpg" alt />
          </div>
          <div class="contentDescription">
            <h3 class="subTitle">contrução civil</h3>
            <p></p>
          </div>
        </article>
      </router-link>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.backgroundNo {
  background-image: url("../assets/grupo25.svg");
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
  justify-content: space-between;
}

.cards {
  margin: 0 50px;
  align-items: center;
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
.tituloNo {
  color: rgb(232, 76, 61);
  font-weight: 800;
  font-size: 2rem;
  text-align: start;
  margin-left: 50px;
  text-transform: uppercase;
}
.contentDescription {
  background: rgb(4, 85, 125);
  color: rgb(255, 255, 255);
  padding: 15px 5px;
  align-items: stretch;
}

.contentDescription p {
  margin: 0;
  padding: 0;
}

.contentImagem {
  margin-bottom: -6px;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .backgroundNo {
    background-size: cover;
    height: auto;
  }
  .backgroundNo h1.tituloNo {
    color: #fff;
  }
  .backgroundNo .cards {
    flex-wrap: wrap;
    margin: 0 15px;
  }
  h1.tituloNo {
    margin-left: 15px;
  }
  .cards a {
    margin-bottom: 20px;
  }
}
/* 
@media screen and (max-width: 1000px) {
  img,
  .contentImagem {
    display: flex;
    flex-wrap: wrap;
  }
}
@media screen and (max-width: 990px) {
  .contentDescription,
  .cards {
    display: flex;
  }
}
@media screen and (max-width: 990px) {
  a,
  .cards {
    width: 100%;
    align-items: flex-start;
  }
  p {
    display: none;
  }
  .subTitle {
    font-size: 1rem;
  }
} */

/* @media screen and (max-width: 1000px) {
  .backgroundNo {
    background-repeat: repeat;
  }
}
@media screen and (max-width: 1000px) {
  h1,
  .titutloNo {
    color: rgb(255, 255, 255) !important;
  }
}

@media screen and (max-width: 550px) {
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
}
@media screen and (max-width: 550px) {
  .card {
    flex: 0 1 40%;
  }
} */
</style>
