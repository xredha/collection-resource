<template>
  <ul>
    <li>{{storedResource[0].title}}</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      storedResource: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          desc: 'You must learn Vue JS in this website',
          link: 'https://vuejs.org/'
        },
        {
          id: 'google',
          title: 'Google',
          desc: 'Learn programming in Google',
          link: 'https://google.com/'
        },
      ]
    }
  }
}
</script>

<style>

</style>