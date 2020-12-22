<template lang="pug">
  .home
    //- img(alt="Vue logo" src="../assets/logo.png")
    Cover(msg="Welcome to Your Vue.js App")
    Intro
    News
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Cover from '@/components/cover.vue'
import Intro from '@/components/intro.vue'
import News from '@/components/news.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Cover,
    Intro,
    News
  }
}
</script>
