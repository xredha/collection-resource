<template>
  <base-card>
    <base-button
      @click="setSelectedComponent('stored-resource')"
      :mode="onSelectedTab('stored-resource')"
      >Stored Resource</base-button
    >
    <base-button
      @click="setSelectedComponent('add-resource')"
      :mode="onSelectedTab('add-resource')"
      >Add Resource</base-button
    >
  </base-card>
  <component :is="selectedComponent"></component>
</template>

<script>
import AddResource from "./AddResource.vue";
import StoredResource from "./StoredResource.vue";

export default {
  components: {
    AddResource,
    StoredResource,
  },
  data() {
    return {
      selectedComponent: "stored-resource",
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
  methods: {
    setSelectedComponent(cmp) {
      this.selectedComponent = cmp;
    },
    onSelectedTab(cmp) {
      return this.selectedComponent === cmp ? null : "flat";
    },
  },
  provide() {
    return {
      resources: this.storedResource,
    };
  },
};
</script>

<style scoped>
</style>