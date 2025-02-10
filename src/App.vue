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
      iframeSrc: "https://embeds.beehiiv.com/bee58212-55f9-4f7c-994e-380751e3d646", // Initial source
    };
  },
};
</script>

<style>
/* Ensure the app container and iframe cover the entire viewport */
html, body, #app, iframe {
  margin: 0;
  padding: 0;
  width: 100vw; /* Full width */
  height: 100vh; /* Full height */
  overflow: hidden;
  border: none;
}

/* Set a background image */
body {
  background: url('/cool.png') no-repeat center center fixed;
  background-size: cover;
}
</style>
