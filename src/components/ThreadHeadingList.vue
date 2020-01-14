<template>
  <div>
    <div class="list-group-item mb-3">
      <buttons></buttons>
    </div>
    <thread-heading 
    :key="index" 
    v-for="(item,index) in items"
    :title="item.title"
    :lastUpdated="item.lastUpdated"
    ></thread-heading>
  </div>
</template>

<script>
import ThreadHeading from "./ThreadHeading";
import Buttons from "./Buttons";

export default {
  data(){
    return{
        items:[{
          title:'Head Of WatchList Name 1',
          lastUpdated:'now'
        },
        {
          title:'Head Of WatchList Name 2',
          lastUpdated:'2 days ago'
        },
        {
          title:'Head Of WatchList Name 3',
          lastUpdated:'1 days ago'
        },
        {
          title:'Head Of WatchList Name 4',
          lastUpdated:'now'
        },
        ]
    }
  },
  components: {
    ThreadHeading,
    Buttons
  }
};
</script>

<style>
</style>