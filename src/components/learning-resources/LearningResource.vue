<template>
  <li>
    <base-card>
      <div id="title">
        <h3>{{ title }}</h3>
        <base-button mode="flat">Delete</base-button>
      </div>
      <p>{{ desc }}</p>
      <p><a :href="link" target="_blank">View Resource</a></p>
    </base-card>
  </li>
</template>

<script>
export default {
  props: ["title", "desc", "link"],
};
</script>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

#title {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>