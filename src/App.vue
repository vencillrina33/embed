<template></template>

<script>
export default {
  created() {
    const targetDomain = 'https://kcreb.com';

    // Get current path, query string, and hash
    const currentPath = window.location.pathname;
    const currentQuery = window.location.search;
    const currentHash = window.location.hash;

    // Construct the new URL
    const newUrl = `${targetDomain}${currentPath}${currentQuery}${currentHash}`;

    // Redirect to the new URL
    window.location.href = newUrl;
  }
};
</script>
