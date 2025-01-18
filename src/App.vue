<template>
  <div id="app">
    <div class="iframe-container">
      <iframe
        src="https://embeds.beehiiv.com/bee58212-55f9-4f7c-994e-380751e3d6"
        data-test-id="beehiiv-embed"
        width="100%"
        height="320"
        frameborder="0"
        scrolling="no"
        style="border-radius: 4px; border: 2px solid #e5e7eb; background-color: transparent;">
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
#app {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f9fafb;
}
.iframe-container {
  width: 100%;
  max-width: 800px; /* Adjust the max width as needed */
  margin: 0 auto;
}
</style>
