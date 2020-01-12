<template>
  <div>
    <buttonWhatsapp />
    <inicio />
    <sobrenos />
    <nosos />
    <realizacoes />
    <contato />
    <rodape />
  </div>
</template>

<script>
import buttonWhatsapp from "@/components/buttonWhatsapp.vue";

import inicio from "@/components/inicio.vue";
import sobrenos from "@/components/sobrenos.vue";
import nosos from "@/components/nosos.vue";
import realizacoes from "@/components/realizacoes.vue";
import contato from "@/components/contato.vue";
import rodape from "@/components/rodape.vue";
// import GoogleMapLoader from './components/GoogleMapLoader.vue'

export default {
  name: "app",
  components: {
    buttonWhatsapp,
    inicio,
    sobrenos,
    nosos,
    realizacoes,
    contato,
    rodape
  }
};
</script>

<style>
</style>