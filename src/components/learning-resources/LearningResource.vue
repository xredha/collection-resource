<template>
  <li>
    <div id="title">
      <h1>{{ title }}</h1>
      <button>Delete</button>
    </div>
    <p>{{ desc }}</p>
    <p><a :href="link">View Resource</a></p>
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