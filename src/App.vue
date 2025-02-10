<template>
  <div id="app">
    <iframe
      :src="iframeSrc"
      frameborder="0"
      scrolling="no"
      seamless>
    </iframe>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      iframeSrc: "https://3dp5fc-8080.csb.app/",
    };
  },
};
</script>

<style>
/* Ensure there is absolutely no margin, padding, or gaps */
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

#app {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: url('/cool.png') no-repeat center center fixed;
  background-size: cover;
}

/* Ensure the iframe takes up the full viewport */
iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  border: none;
}
</style>
