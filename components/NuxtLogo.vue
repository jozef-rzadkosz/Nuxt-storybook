<template>
  <div class='nuxt-logo'>
    <span class='nuxt-logo__title'>NuxtLogo</span>
    <img class='nuxt-logo__image' :src='image' alt=''>
    <code>{{multiply({x: 2, y: 15})}}</code>
  </div>
</template>

<script lang='ts'>
interface Numbers {
  x: number,
  y: number,
}

export default {
  props: {
    image: {
      type: [String]
    }
  },
  methods: {
    multiply(coords: Numbers):number {
      return coords.x * coords.y;
    }
  }
}
</script>

<style lang='scss' scoped>
.nuxt-logo {
  height: 180px;
  &__title{
    font-size: 2rem;
  }
  &__image{
    width: 500px;
  }
}
</style>
