<template>
  <section id="sobre" class="flex">
    <div class="textoSobre flex2">
      <h1 class="titulos">sobre nós</h1>
      <p class="blocktext">
        Empresa no Ramo de Construções e Reformas fundada
        <br />desde 2005, com varias obras ja feitas do alicerce
        <br />ao acabamento, pintura, elétrica, hidráulica, pisos, azulejos,
        <br />porcelanato, pedras, telhados, lajes, demolição, serviços
        <br />com garantia e sempre oferecendo o melhor aos seus
        <br />clientes e amigos . Venha nos fazer um orçamento sem compromisso
        <br />estamos aqui para ajudar no que for necessario.
        <br />Desde ja agradecemos a preferencia.M&M Construções e Reformas.
      </p>
      <br />
    </div>
    <div class="flex1">
      <div class="fotoSobre">
          <div class="bordaEspecial">
              <img class="img-responsive" src="@/assets/fotoSobre.jpg" alt />
          </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "sobrenos",
  data: () => {
    return {
      ano: 2019
    };
  }
};
</script>

<style>
#sobre {
  align-items: center;
  background-color: #f7f7f7;
  background-image: linear-gradient(to right, #f7f7f7 80%, #fff 20%);
}
.textoSobre {
  flex-direction: column;
  height: 100vh;
}
.fotoSobre img {
  z-index: 1;
  max-width: 25vw;
  margin-right: 10vw;
}
.bordaEspecial{
    border:2px solid #f7f;
    padding-top: 5px;
    padding-right: 5px;
    padding-bottom: -10px;
}


p.blocktext {
  margin-left: 50px;
  /* margin-right: auto; */
  /* width: 6em  */
  text-align: left;
  text-align: justify;
  margin-top: 50px;
  margin-bottom: 0;
}
</style>