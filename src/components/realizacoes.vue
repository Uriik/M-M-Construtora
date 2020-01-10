<template>
  <section class="backgroundRe flex column center flex-start">
    <div class="flex-start">
      <div class="flex0">
        <!-- ARRUMAR A FLEX0 -->
        <h1 class="titulos">realizações da empresa</h1>
      </div>
    </div>

    <div class="testando grid">
      <div class>
        <div class="container-test">
          <div class="test1">
            <img src="@/assets/realizacoes/cacavz.jpg" class="img-figure" />
            <div>
              <h4 class="titulo1">lorem ipsum</h4>
            </div>
          </div>

          <div class="test2">
            <img src="@/assets/realizacoes/pintura.jpg" class="img-figure" />
            <div>
              <h4 class="titulo2">lorem ipsum</h4>
            </div>
          </div>

          <div class="test3">
            <img src="@/assets/realizacoes/alicerce.jpg" class="img-figure" />
            <div>
              <h4 class="titulo3">lorem ipsum</h4>
            </div>
          </div>

          <div class="test4">
            <img src="@/assets/realizacoes/caminho1415.jpg" class="img-figure" />
            <div>
              
            </div>
          </div>

          <div class="test5">
            <img src="@/assets/realizacoes/hidraulica.jpg" class="img-figure" />
            <div>
              <h4 class="titulo5">lorem ipsum</h4>
            </div>
          </div>

          <div class="test6">
            <img src="@/assets/realizacoes/eletrica.jpg" class="img-figure" />
            <div>
              <h4 class="titulo6">lorem ipsum</h4>
            </div>
          </div>

          <div class="test7">
            <img src="@/assets/realizacoes/acabamentos.jpg" class="img-figure" />
            <div>
              <h4 class="titulo7">lorem ipsum</h4>
            </div>
          </div>

          <div class="test8">
            <img src="@/assets/realizacoes/alvenaria.jpg" class="img-figure" />
            <div>
              <h4 class="titulo8">lorem ipsum</h4>
            </div>
          </div>

          <div class="test9">
            <img src="@/assets/realizacoes/pisos.jpg" class="img-figure" />
            <div>
              <h4 class="titulo9">lorem ipsum</h4>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.backgroundRe {
  background-image: url("../assets/grupo35.svg");
  background-repeat: no-repeat;
  background-size: cover;
}

.testando {
  height: 70vh;
  margin-left: 50px;
}

.grid {
  display: grid;
}

.testando2 {
  border: 1px solid pink;
  height: 500px;
  width: 1250px;
}

@media (min-width: 600px) {
  .container-test {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(6, 10vh);
    row-gap: 0.5em;
    column-gap: 0.5em;
    position: relative;
    width: 200vh;
  }
}

.flex {
  display: flex;
}

.titulo1,
.titulo2,
.titulo3,
.titulo5,
.titulo6,
.titulo7,
.titulo8,
.titulo9 {
  position: absolute;
  bottom: 0px;
  width: 100%;
  padding: 30px;
  background: rgba(0, 0, 0, 0);
  background: -moz-linear-gradient(
    top,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 1) 100%
  );
  background: -webkit-gradient(
    left top,
    left bottom,
    color-stop(0%, rgba(0, 0, 0, 0)),
    color-stop(100%, rgba(0, 0, 0, 1))
  );
  background: -webkit-linear-gradient(
    top,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 1) 100%
  );
  background: -o-linear-gradient(
    top,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 1) 100%
  );
  background: -ms-linear-gradient(
    top,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 1) 100%
  );
  background: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 1) 100%
  );
  width: 100%;
  text-align: left;
  color: #fff;
}

h4 {
  margin: 0;
}

@media (min-width: 600px) {
  .test1,
  .titulo1 {
    grid-column: 1/3;
    grid-row: 1/7;
  }
}

.img-figure {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (min-width: 600px) {
  .test2,
  .titulo2 {
    grid-column: 3/7;
    grid-row: 1/4;
  }
}

@media (min-width: 600px) {
  .test3,
  .titulo3 {
    grid-column: 3/5;
    grid-row: 4/7;
  }
}
@media (min-width: 600px) {
  .test4,
  .titulo4 {
    grid-column: 5/7;
    grid-row: 4/7;
  }
}

@media (min-width: 600px) {
  .test5,
  .titulo5 {
    grid-column: 7/9;
    grid-row: 1/4;
  }
}

@media (min-width: 600px) {
  .test6,
  .titulo6 {
    grid-column: 7/9;
    grid-row: 4/7;
  }
}
@media (min-width: 600px) {
  .test7,
  .titulo7 {
    grid-column: 9/11;
    grid-row: 1/4;
  }
}
@media (min-width: 600px) {
  .test8,
  .titulo8 {
    grid-column: 9/11;
    grid-row: 4/7;
  }
}
@media (min-width: 600px) {
  .test9,
  .titulo9 {
    grid-column: 11/13;
    grid-row: 1/7;
  }
}
</style>