<template>
  <div class="home">
    <img alt="Vue logo" src="@/assets/martillos.jpg">
    <HelloWorld msg="Bienvenido al carrito"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
<style lang="scss" scoped>
img{
  max-width: 200px;
}
</style>
