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
    <div class="controls">
      <button @click="updateIframe('https://embeds.beehiiv.com/bee58212-55f9-4f7c-994e-380751e3d6')">
        Load Beehiiv
      </button>
      <button @click="updateIframe('https://example.com')">
        Load Example
      </button>
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
  methods: {
    updateIframe(newSrc) {
      this.iframeSrc = newSrc; // Dynamically update iframe source
    },
  },
};
</script>

<style>
/* Ensure the app container fills the entire viewport */
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100vw; /* Full width of the viewport */
  height: 100vh; /* Full height of the viewport */
  margin: 0;
  background-color: #f9fafb;
  overflow: hidden; /* Prevent scrollbars in the app */
}

/* Make the iframe responsive and full-screen */
.iframe-container {
  width: 100%; /* Full width */
  height: 90%; /* Most of the height */
  overflow: hidden; /* Prevent scrollbars inside the iframe container */
}

.iframe-container iframe {
  width: 100%; /* Match container's width */
  height: 100%; /* Match container's height */
  border: 0; /* Remove border */
  background-color: transparent;
  overflow: hidden; /* Prevent scrollbars */
}

/* Add styling for controls */
.controls {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  height: 10%; /* Reserve space for controls */
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #4CAF50;
  color: white;
  cursor: pointer;
  font-size: 16px;
}

button:hover {
  background-color: #45a049;
}
</style>
