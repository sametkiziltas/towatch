<template>
  <div class="list-group-item list-group-item-action flex-column align-items-start mb-2">
    <div class="justify-content-center">
      <h6 class="mb-1 justify-content-left">{{ title }}</h6 >
       <small> {{ lastUpdated }}</small>
    </div>

  </div>
</template>

<script>
export default {
  props:{
    title:{
      type:String,
      required:true
    },
    lastUpdated:{
      type:String,
      required:true
    }
  }
};
</script>
<style scoped>

</style>