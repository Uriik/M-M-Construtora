<template>
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
</template>


<script>
export default {};
</script>

<style>
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

.dev {
  text-align: right;
}

.meu-nome {
  font-weight: bold;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  footer.rodape {
    height: auto;
    flex-direction: column;
  }
  footer.rodape .dev {
    text-align: center;
  }
}
</style>