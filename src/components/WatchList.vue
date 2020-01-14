<template>
  <div>
    <div>
      <div class="list-group-item mb-3">
        <buttons></buttons>
      </div>
    </div>
    <watch :key="index" v-for="(item,index) in 10"></watch>
  </div>
</template>

<script>
import Watch from "./Watch";
import Buttons from "./Buttons";

export default {
  components: {
    Watch,
    Buttons
  }
};
</script>

<style>
</style>