<template>
  <div id="app">
    <div class="iframe-container">
      <iframe
        :src="iframeSrc"
        frameborder="0"
        scrolling="no"
        seamless>
      </iframe>
    </div>
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
/* Ensure the app container fills the entire viewport */
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw; /* Full width of the viewport */
  height: 100vh; /* Full height of the viewport */
  margin: 0;
  background: url('/background.jpg') no-repeat center center; /* Background image */
  background-size: cover; /* Make the image cover the entire container */
  overflow: hidden; /* Prevent scrollbars in the app */
}

/* Make the iframe responsive and full-screen */
.iframe-container {
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: hidden; /* Prevent scrollbars inside the iframe container */
}

.iframe-container iframe {
  width: 100%; /* Match container's width */
  height: 100%; /* Match container's height */
  border: 0; /* Remove border */
  background-color: transparent;
  overflow: hidden; /* Prevent scrollbars */
}
</style>
