<template>
  <div>
    <div class="avatar">
      <img :width="size" :height="size" :src="source" alt="">
    </div>
  </div>
</template>

<script>
  export default {
    props:{
      size:String,
      source:String,
    }
  }
</script>

<style lang="scss" scoped>
img{
  border-radius: 50%;
}
</style>