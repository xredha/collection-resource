<template>
  <the-header :title="'Collection Resource'"></the-header>
  <the-resources></the-resources>
  <the-footer
    :contribute="'Galih Redha Saputra'"
    :link="'https://github.com/xredha'"
  ></the-footer>
</template>

<script>
import TheHeader from "./components/layouts/TheHeader.vue";
import TheResources from './components/learning-resources/TheResources.vue';
import TheFooter from "./components/layouts/TheFooter.vue";

export default {
  components: {
    TheHeader,
    TheResources,
    TheFooter,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

* {
  box-sizing: border-box;
}

html {
  font-family: "Roboto", sans-serif;
}

body {
  margin: 0;
}
</style>