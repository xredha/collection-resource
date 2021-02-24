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
  <keep-alive>
    <component :is="selectedComponent"></component>
  </keep-alive>
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
    addResource(title, desc, link) {
      const newResource = {
        id: new Date().toISOString(),
        title: title,
        desc: desc,
        link: link,
      };
      this.storedResource.unshift(newResource);
      this.selectedComponent = "stored-resource";
    },
  },
  provide() {
    return {
      resources: this.storedResource,
      addResource: this.addResource,
    };
  },
};
</script>

<style scoped>
</style>