<template>
  <div class="item">
    <div>
      <button class="btn btn-primary" @click="onAddClick">{{showSave ? 'Save' : 'Add New'}}</button>
    </div>
    <div>
      <button
        type="button"
        class="btn"
        :class="modeChange[1]"
        @click="onEditClick()"
      >Edit: {{ modeChange[0] }}</button>
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
  props: {
    showSave: {
      type: Boolean
    }
  },
  computed: {
    modeChange() {
      if (this.mode) {
        return ["On", "btn-success"];
      }
      return ["Off", "btn-danger"];
    }
  },
  methods: {
    onAddClick() {
      let type = this.showSave ? "save" : "add";
      this.$emit("clicked", { type });
    },
    onEditClick() {
      this.mode = !this.mode;
      this.$emit("clicked", { type: "edit", mode: this.mode });
    }
  }
};
</script>

<style scoped>
.item {
  display: flow-root;
}
.item button {
  float: right;
  margin-left: 5px;
}
</style>