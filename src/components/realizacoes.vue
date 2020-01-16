<template>
  <section class="backgroundRe flex column center flex-start">
    <div class="flex-start">
      <div class="flex0">
        <!-- ARRUMAR A F-->
        <h1 class="titulos">realizações da empresa</h1>
      </div>
    </div>

    <div class="testando grid">
      <div>
        <!-- <button @click="showSingle">Show single picture.</button>
        <button @click="showMultiple">Show a group of pictures.</button>-->
        <VueEasyLightbox :visible="visible" :imgs="imgs" :index="index" @hide="handleHide"></VueEasyLightbox>
      </div>
      <div class>
        <div class="container-test">
          <div class="test1" @click="showMultiple(0)">
            <img src="@/assets/realizacoes/cacavz.jpg" class="img-figure" />
            <div>
              <h4 class="titulo1">Caça Vazamentos</h4>
            </div>
          </div>

          <div class="test2" @click="showMultiple(1)">
            <img src="@/assets/realizacoes/pintura.jpg" class="img-figure" />
            <div>
              <h4 class="titulo2">Pintura</h4>
            </div>
          </div>

          <div class="test3" @click="showMultiple(2)">
            <img src="@/assets/realizacoes/alicerce.jpg" class="img-figure" />
            <div>
              <h4 class="titulo3">Alicerces</h4>
            </div>
          </div>

          <div class="test4">
            <img src="@/assets/realizacoes/caminho1415.jpg" class="img-figure" />
            <div></div>
          </div>

          <div class="test5" @click="showMultiple(4)">
            <img src="@/assets/realizacoes/hidraulica.jpg" class="img-figure" />
            <div>
              <h4 class="titulo5">Hidraulica</h4>
            </div>
          </div>

          <div class="test6" @click="showMultiple(5)">
            <img src="@/assets/realizacoes/eletrica.jpg" class="img-figure" />
            <div>
              <h4 class="titulo6">Eletrica</h4>
            </div>
          </div>

          <div class="test7" @click="showMultiple(6)">
            <img src="@/assets/realizacoes/acabamentos.jpg" class="img-figure" />
            <div>
              <h4 class="titulo7">Acabamentos</h4>
            </div>
          </div>

          <div class="test8" @click="showMultiple(7)">
            <img src="@/assets/realizacoes/alvenaria.jpg" class="img-figure" />
            <div>
              <h4 class="titulo8">Alvenaria</h4>
            </div>
          </div>

          <div class="test9" @click="showMultiple(8)">
            <img src="@/assets/realizacoes/pisos.jpg" class="img-figure" />
            <div>
              <h4 class="titulo9">Pisos</h4>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mobile-list">
      <div>
        <!-- <button @click="showSingle">Show single picture.</button>
        <button @click="showMultiple">Show a group of pictures.</button>-->
        <VueEasyLightbox :visible="visible" :imgs="imgs" :index="index" @hide="handleHide"></VueEasyLightbox>
      </div>
      <article @click="showMultiple(0)">
        <h4 class>Caça Vazamentos</h4>
      </article>
      <article @click="showMultiple(1)">
        <h4 class>Pintura e texturas</h4>
      </article>
      <article @click="showMultiple(2)">
        <h4 class>Alicerces</h4>
      </article>
      <article @click="showMultiple(4)">
        <h4>Hidraulica</h4>
      </article>
      <article @click="showMultiple(5)">
        <h4>Eletrica</h4>
      </article>
      <article @click="showMultiple(6)">
        <h4>Acabamentos</h4>
      </article>
      <article @click="showMultiple(7)">
        <h4>Alvenaria</h4>
      </article>
      <article @click="showMultiple(8)">
        <h4>Pisos</h4>
      </article>
    </div>
  </section>
</template>

<script>
import VueEasyLightbox from "vue-easy-lightbox";

export default {
  data() {
    return {
      imgs: "", // Img Url , string or Array
      visible: false,
      index: 0 // default
    };
  },
  components: {
    VueEasyLightbox
  },
  methods: {
    showSingle() {
      this.imgs = "http://via.placeholder.com/350x150";
      this.show();
    },
    showMultiple(numCat) {
      this.imgs = [
        // 0 = caça vazamento
        [
          require("../assets/realizacoes/cacavz/caca1.jpg"),
          require("../assets/realizacoes/cacavz/caca2.jpg")
        ],

        // 1 = pintura
        [
          require("../assets/realizacoes/pintura/pint1.jpg"),
          require("../assets/realizacoes/pintura/pint2.jpg"),
          require("../assets/realizacoes/pintura/pint3.jpg"),
          require("../assets/realizacoes/pintura/pint4.jpg"),
          require("../assets/realizacoes/pintura/pint5.jpg")
        ],
        // 2 = alicerces
        [
          require("../assets/realizacoes/alicerce/alice1.jpg"),
          require("../assets/realizacoes/alicerce/alice1.jpg")
        ],

        // 3 = balela
        [require("../assets/realizacoes/alicerce/alice1.jpg")],
        // 4 = hidraulica
        [
          require("../assets/realizacoes/hidraulica/hid1.jpg"),
          require("../assets/realizacoes/hidraulica/hid2.jpg"),
          require("../assets/realizacoes/hidraulica/hid3.jpg")
        ],

        // 5 = elétrica
        [
          require("../assets/realizacoes/acabamentos/acab1.jpg"),
          require("../assets/realizacoes/acabamentos/acab1.jpg")
        ],

        // 6 = acabamentos
        [
          require("../assets/realizacoes/acabamentos/acab1.jpg"),
          require("../assets/realizacoes/acabamentos/acab2.jpg"),
          require("../assets/realizacoes/acabamentos/acab3.jpg"),
          require("../assets/realizacoes/acabamentos/acab4.jpg")
        ],

        [
          // 7 = alvenaria
          require("../assets/realizacoes/alvenaria/alv1.jpg"),
          require("../assets/realizacoes/alvenaria/alv1.jpg")
        ],

        [
          // 8 = pisos
          require("../assets/realizacoes/pisos/pis1.jpg"),
          require("../assets/realizacoes/pisos/pis2.jpg"),
          require("../assets/realizacoes/pisos/pis3.jpg"),
          require("../assets/realizacoes/pisos/pis4.jpg"),
          require("../assets/realizacoes/pisos/pis5.jpg")
        ]
      ];

      this.imgs = this.imgs[numCat];
      this.index = 1; // index of imgList
      this.show();
    },
    show() {
      this.visible = true;
    },
    handleHide() {
      this.visible = false;
    }
  }
};
</script>

<style>
.backgroundRe {
  background-image: url("../assets/grupo35.svg");
  background-repeat: no-repeat;
  background-size: cover;
}
.mobile-list {
  display: none;
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

.container-test {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(6, 10vh);
  row-gap: 0.5em;
  column-gap: 0.5em;
  position: relative;
  width: 200vh;
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

.test1,
.titulo1 {
  grid-column: 1/3;
  grid-row: 1/7;
}

.img-figure {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.test2,
.titulo2 {
  grid-column: 3/7;
  grid-row: 1/4;
}

.test3,
.titulo3 {
  grid-column: 3/5;
  grid-row: 4/7;
}

.test4,
.titulo4 {
  grid-column: 5/7;
  grid-row: 4/7;
}

.test5,
.titulo5 {
  grid-column: 7/9;
  grid-row: 1/4;
}

.test6,
.titulo6 {
  grid-column: 7/9;
  grid-row: 4/7;
}

.test7,
.titulo7 {
  grid-column: 9/11;
  grid-row: 1/4;
}

.test8,
.titulo8 {
  grid-column: 9/11;
  grid-row: 4/7;
}

.test9,
.titulo9 {
  grid-column: 11/13;
  grid-row: 1/7;
}

@media screen and (max-width: 1300px) {
  .container-test {
    width: 90%;
    height: 90%;
  }
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .backgroundRe {
    height: auto;
  }
  .mobile-list {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding: 15px;
  }
  .mobile-list article {
    padding: 20px;
    background-color: #e84c3d;
    flex: 1;
    color: #fff;
    margin-bottom: 5px;
  }
  .mobile-list article h4 {
    text-align: left;
  }
  .backgroundRe .testando {
    display: none;
  }
  h1.titulos {
    margin-left: 15px;
  }
}

/* @media screen and (max-width:1000px ){
    .titulo1,.titulo2,.titulo3,.titulo4,.titulo5,.titulo6,.titulo7,.titulo8,.titulo9{
       width: 90%;
      height: 90%;
    }
  }   */
</style>
