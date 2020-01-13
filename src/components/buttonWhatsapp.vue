<template>
  <div class="whatsapp">
    <a href="https://api.whatsapp.com/send?phone=5513974142011&text=Olá,%20meu%20friendo!">
      <img src="@/assets/ic-whatsapp.png" alt />
    </a>
  </div>
</template>
<script>
export default {
  name: "whatsapp"
};
</script>
<style>
.whatsapp {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: #fff;
  width: 70px;
  height: 70px;
  border-radius: 50%;
  padding: 10px;
  z-index: 9999999;
  -webkit-box-shadow: -3px 3px 10px 0px rgba(0, 0, 0, 0.64);
  -moz-box-shadow: -3px 3px 10px 0px rgba(0, 0, 0, 0.64);
  box-shadow: -3px 3px 10px 0px rgba(0, 0, 0, 0.64);
}
.whatsapp img {
  width: 100%;
  height: auto;
}
</style>