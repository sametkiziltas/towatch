<template>
  <div class="item">
    <div>
      <button class="btn btn-primary">Add</button>
    </div>
    <div>
      <button
        type="button"
        class="btn"
        :class="changeButton[1]"
        @click="mode = !mode"
      >Edit: {{ changeButton[0] }}</button>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      mode: false,
      text: "Off"
    };
  },
  computed: {
    changeButton: function() {
      if (this.mode) {
        return ["On", "btn-success"];
      } else {
        return ["Off", "btn-danger"];
      }
    }
  }
};
</script>

<style scoped>
.item {
  display: grid;
}
.item button {
  float: right;
  margin-left: 5px;
}
</style>