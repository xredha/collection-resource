<template>
  <ul>
    <learning-resource
      v-for="rsc in resources"
      :key="rsc.id"
      :id="rsc.id"
      :title="rsc.title"
      :desc="rsc.desc"
      :link="rsc.link"
    ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from "./LearningResource.vue";

export default {
  components: {
    LearningResource,
  },
  inject: ["resources"],
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>