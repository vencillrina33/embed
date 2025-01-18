<template>
  <div id="app">
    <div class="iframe-container">
      <iframe
        src="https://embeds.beehiiv.com/bee58212-55f9-4f7c-994e-380751e3d646"
        data-test-id="beehiiv-embed"
        frameborder="0"
        scrolling="no">
      </iframe>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
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
  background-color: #f9fafb;
}

/* Make the iframe responsive and full-screen */
.iframe-container {
  width: 100%; /* Take up full width */
  height: 100%; /* Take up full height */
}

.iframe-container iframe {
  width: 100%; /* Match container's width */
  height: 100%; /* Match container's height */
  border-radius: 0; /* Optional: Remove border radius for fullscreen */
  border: 0; /* Optional: Remove iframe border for clean look */
  background-color: transparent;
}
</style>
