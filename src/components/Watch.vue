<template>
  <div class="list-group-item list-group-item-action flex-column align-items-start mb-3" v-if="url">
    <div class="d-flex w-100 justify-content-between">
      <h5 class="mb-1">{{ title }}</h5>
      <small>{{ lastUpdated }}</small>
    </div>
    <div class="embed-container">
      <iframe
        :src="url"
        frameborder="0"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
    <p class="mb-1">{{ desc }}</p>
  </div>
  <div class="list-group-item list-group-item-action flex-column align-items-start mb-3" v-else>
    {{url}}
    <input class="form-control mb-1" type="text" placeholder="URL"/>
    <input class="form-control mb-1" type="text" placeholder="Head"/>
    <input class="form-control mb-1" type="text" placeholder="Description"/>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    },
    url: {
      type: String,
      required: true
    },
    desc: {
      type: String
    },
    lastUpdated: {
      type: String
    },
    showSave:{
      type:Boolean,
      required:true
    }
  },
};
</script>
<style scoped>
.embed-container {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
  overflow: hidden;
  max-width: 100%;
  margin: 10px;
}
.embed-container iframe,
.embed-container object,
.embed-container embed {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.list-group {
  top: 50%;
  left: 50%;
  display: inline;
  margin: 0 auto;
}
</style>