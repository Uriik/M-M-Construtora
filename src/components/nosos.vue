<template>
  <section class="column flex backgroundNo" id="nossosServicos">
    <div class="flex0">
      <h1 class="titulos">nossos serviços</h1>
    </div>
    <div class="flex flex1 cards">
      <router-link to="/detalhes/0" class="card flex1">
        <article>
          <div class="contentImagem">
            <img class="img-responsive" src="@/assets/servicos/caca.jpg" alt />
          </div>
          <div class="contentDescription">
            <h3 class="subTitle">caça vazamentos</h3>
            <p>Lorem Ipsum</p>
          </div>
        </article>
      </router-link>
      <router-link to="/detalhes/1" class="card flex1">
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
      </router-link>
      <router-link to="/detalhes/2" class="card flex1">
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
      </router-link>
      <router-link to="/detalhes/3" class="card flex1">
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

@media(max-width:875px ){
    
}
</style>
