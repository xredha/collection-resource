<template>
  <the-header :title="'Collection Resource'"></the-header>
  <stored-resource :resources="storedResource"></stored-resource>
  <the-footer
    :contribute="'Galih Redha Saputra'"
    :link="'https://github.com/xredha'"
  ></the-footer>
</template>

<script>
import TheHeader from "./components/layouts/TheHeader.vue";
import StoredResource from "./components/learning-resources/StoredResource.vue";
import TheFooter from "./components/layouts/TheFooter.vue";

export default {
  components: {
    TheHeader,
    StoredResource,
    TheFooter,
  },
  data() {
    return {
      storedResource: [
        {
          id: "official-guide",
          title: "Official Guide",
          desc: "You must learn Vue JS in this website",
          link: "https://vuejs.org/",
        },
        {
          id: "google",
          title: "Google",
          desc: "Learn programming in Google",
          link: "https://google.com/",
        },
      ],
    };
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