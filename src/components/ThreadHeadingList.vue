<template>
  <div>
    <div class="list-group-item mb-3">
      <buttons></buttons>
    </div>
    <thread-heading :key="index" v-for="(item,index) in 10"></thread-heading>
  </div>
</template>

<script>
import ThreadHeading from "./ThreadHeading";
import Buttons from "./Buttons";

export default {
  components: {
    ThreadHeading,
    Buttons
  }
};
</script>

<style>
</style>