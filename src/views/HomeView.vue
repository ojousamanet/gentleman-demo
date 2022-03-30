<template>
  <div class="home">
    <div class="container">
      <div class="px-5 py-2">
        <img alt="site logo" src="@/assets/men.svg">
      </div>
    </div>
    <HelloWorld msg="風俗紳士倶楽部"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
