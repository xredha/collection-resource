<template>
  <header>
    <p>2021 &copy; <a :href="link" target="_blank">{{contribute}}</a> Made with ❤️</p>
  </header>
</template>

<script>
export default {
  props: ['link','contribute']
}
</script>

<style scoped>
header {
  width: 100%;
  height: 4rem;
  background-color: #36c2e9;
  display: flex;
  justify-content: center;
  align-items: center;
}

header p {
  color: white;
  margin: 0;
}

a {
  text-decoration: none;
  color: rgba(0, 0, 0, 0.5);
}

a:hover,
a:active {
  color: rgba(0, 0, 0, 0.75);
}
</style>