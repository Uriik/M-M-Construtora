<template>
  <header class="v-header container">
    <div class="fullscreen-video-wrap">
      <video  src="@/assets/videobg.mp4" autoplay="true" loop="true" playsinline="true" muted="true"></video>
    </div>
    <div class="header-overlay"></div>
    <div class="header-content">
      <h1>M&M</h1>
      <p class="ref">Construções e Reformas</p>
      <p class="cubo">Lorem Ipsum is simply dummy</p>
      <p class="monte">Lorem Ipsum is simply dummy</p>
    </div>

  </header>
</template>

<script>
export default {
  name: "inicio",
  data: () => {
    return {
      ano: 2019
    };
  }
};
</script>

<style scoped>


.cubo {
  margin-top: 20px;
  font-weight: 800;
  font-size: 3rem;
}
.monte {
  color: rgb(232, 76, 61);
  font-style: italic;
  font-size: 1.4rem;
}

.ref {
  margin: 0px;
  margin-left: 0;
  font-size: 1.5rem;
}
p{
  margin: 0;

}


.v-header{
  height: 100vh;
  display: flex;
  align-items: center;
  color: #fff;
}

.container{
  max-width: 960px;
  padding-left: 1rem;
  padding-right: 1rem;
  margin:auto;
  text-align:center;
}

.fullscreen-video-wrap{
  position:absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: url("../assets/fotobg.jpg") no-repeat;
  min-width: 100%;
  min-height: 100%;
  object-fit: scale-down;
}

.fullscreen-video-wrap video{
  min-width: 100%;
  min-height: 100%;
}

.header-overlay{
  height: 100vh;
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
  background: rgba(14, 29, 49, 0.8)
}

.header-content{
  z-index: 2;
  display: flex;
  flex-direction: column;
  flex: 1;
}

.header-content h1 {
  font-weight: 800;
  color: rgb(232, 76, 61);
  margin-bottom: 0;
  font-size: 3.0rem;
}


@media(max-width: 960px){
  .container{
    padding-right: 3rem;
    padding-left: 3rem;
  }
}


 </style>