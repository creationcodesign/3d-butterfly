<template>
  <div class="model">
    <div class="txt">
      <h2>3D</h2>
      <h1>Beautiful Butterfly</h1>
      <p>use mouse or finger to resize or rotate 360°</p>
      <img
        src="../assets/img/rotate.png"
        alt="rotate icon"
        width="30"
        id="rotate"
      />
    </div>
    <model-gltf
      src="static/butterfly/butterfly.gltf"
      :backgroundAlpha="bgAlpha"
      :backgroundColor="bgColor"
    >
    </model-gltf>
  </div>
</template>

<script>
import { ModelGltf } from "vue-3d-model";

export default {
  data() {
    return {
      bgColor: "#e7deae",
      bgAlpha: 0.1,
    };
  },
  components: {
    ModelGltf,
  },
};
</script>

<style>
canvas {
  width: 99vw;
  height: 80vh;
  background-image: url("../assets/img/blooming-field.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
.model {
  width: 99vw;
  height: 95vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.txt {
  width: 99vw;
  padding: 0.3rem 1rem;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  text-align: center;
  background-color: rgba(245, 240, 250, 0.692);
  position: relative;
  top: 1rem;
  z-index: 1000;
}
h1 {
  font-size: 1.3em;
}
h2 {
  padding-right: 0.5rem;
}
.txt p {
  margin-left: auto;
  font-size: 0.8em;
}

#rotate {
  animation: rotate 25s linear 0s infinite;
}

@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

@media only screen and (max-width: 550px) {
  .model {
    width: 100vw;
  }
  canvas {
    width: 100vw;
    height: 100vh;
    background-size: cover;
  }
  .txt h1 {
    font-size: 1.2em;
  }
}
</style>