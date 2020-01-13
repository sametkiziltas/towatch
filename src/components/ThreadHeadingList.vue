<template>
  <div>
    <thread-heading :key="index" v-for="(item,index) in 10"></thread-heading>
  </div>
</template>

<script>
import ThreadHeading from './ThreadHeading'

export default {
  components: {
    ThreadHeading,
  },

}
</script>

<style>

</style>