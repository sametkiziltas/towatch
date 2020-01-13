<template>
  <div>
    <watch :key="index" v-for="(item,index) in 10"></watch>
  </div>
</template>

<script>
import Watch from './Watch'

export default {
  components: {
    Watch,
  },
}
</script>

<style>

</style>