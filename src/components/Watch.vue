<template>
  <div class="list-group-item list-group-item-action flex-column align-items-start mb-3">
    <div class="d-flex w-100 justify-content-between">
      <h5 class="mb-1">Head of Video</h5>
      <small>3 days ago</small>
    </div>
    <div class="embed-container">
      <iframe
        src="https://www.youtube.com/embed/tai_A0RwaI4"
        frameborder="0"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
    <p
      class="mb-1"
    >Video açıklaması ...nec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.</p>
  </div>
</template>

<script>
export default {};
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