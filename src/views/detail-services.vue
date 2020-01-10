<template>
  <section class="flex backgrounduni">
      <div class="flex1">
        <div class="fotoVazamento">
          <img src="@/assets/servicos/caca.jpg" alt />
        </div>
      </div>

      <div class="textoVazamentos flex1 ">
          <h1 class="tituloUnico"> caça vazamentos</h1>
          <p class="textoForm">Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
            <br />Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an 
            <br />unknown printer took a galley of type and scrambled it to make a type specimen book. 
            <br />It has survived not only five centuries, but also the leap into electronic typesetting,
            <br /> remaining essentially unchanged. It was popularised in the 1960s with the 
            <br />release of Letraset sheets containing Lorem Ipsum passages, and more recently 
            <br />with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
      </div>
  </section>
</template>
<script>
export default {};
</script>

<style>

.backgrounduni{
  background-image: url("../assets/grupo25.svg");
  background-repeat: no-repeat;
  background-position: left;
  background-size: contain;
  justify-content: space-between;
}

.textoVazamentos {
  flex-direction: column;
  right: 100vh;
}
.textoForm{
  margin-right: 20px;
  text-align: left;
  text-align: justify;
  margin-top: 50px;
  margin-bottom: 0;
}
.fotoVazamento{
  margin-top: 6vh;
  margin-left: 15vh;
  max-width: 100vw;
}

.tituloUnico{
  color: rgb(232, 76, 61);
  font-weight: 800;
  font-size: 2rem;
  text-align: start;
  text-transform: uppercase;
}
</style>