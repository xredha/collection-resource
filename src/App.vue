<template>
  <stored-resource :resources="storedResource"></stored-resource>
</template>

<script>
import StoredResource from "./components/learning-resources/StoredResource.vue";

export default {
  components: {
    StoredResource,
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