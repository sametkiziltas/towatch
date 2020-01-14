<template>
  <div id="app">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-12">
          <div class="msg pt-3 pb-3 mt-3">
            <h3>Message</h3>
          </div>
        </div>
        <div class="col-3 mt-3">
          <thread-heading-list></thread-heading-list>
        </div>
        <div class="col-9 mt-3">
          <watch-list></watch-list>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import WatchList from "./components/WatchList";
import ThreadHeadingList from "./components/ThreadHeadingList";

export default {
  name: "app",
  components: {
    WatchList,
    ThreadHeadingList,
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #212121;
}
body {
  background-color: #212121;
}
.msg {
  background-color: #2c2c2c;
  color: white;
}
.list-group-item {
  background-color: #2c2c2c;
  color: white;
}
.list-group-item:hover {
  background-color: #333;
  color: white;
}
</style>


