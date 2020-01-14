/* eslint-disable no-console */
<template>
  <div>
    <div>
      <div class="list-group-item mb-3">
        <buttons @clicked="clicked" :showSave="showSave"></buttons>
      </div>
    </div>
    <watch
      :key="index"
      v-for="(item,index) in items"
      :title="item.title"
      :url="item.url"
      :desc="item.desc"
      :lastUpdated="item.lastUpdated"
      :showSave="showSave"
    ></watch>
  </div>
</template>

<script>
import Watch from "./Watch";
import Buttons from "./Buttons";

export default {
  data() {
    return {
      showSave: false,
      items: [
        {
          title: "Head of Video 1",
          url: "https://www.youtube.com/embed/tai_A0RwaI4",
          desc:
            "Video açıklaması ...nec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.",
          lastUpdated: "1 days ago"
        },
        {
          title: "Head of Video 2",
          url: "https://www.youtube.com/embed/gs599fIpeZY",
          desc:
            "Video açıklaması ...nec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.",
          lastUpdated: "2 days ago"
        },
        {
          title: "Head of Video 3",
          url: "https://www.youtube.com/embed/tai_A0RwaI4",
          desc:
            "Video açıklaması ...nec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.",
          lastUpdated: "3 days ago"
        },
        {
          title: "Head of Video 4",
          url: "https://www.youtube.com/embed/tai_A0RwaI4",
          desc:
            "Video açıklaması ...nec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.",
          lastUpdated: "4 days ago"
        }
      ]
    };
  },
  components: {
    Watch,
    Buttons
  },
  methods: {
    clicked: function(payload) {
      if (payload.type == "edit") {
        return this.items;
      } else if (payload.type == "add") {
        this.showSave = true;
        return this.items.splice(0, 0, {
          title: "",
          url: "",
          desc: "",
          lastUpdated: ""
        });
      } else if (payload.type == "save") {
        this.showSave = false;
      }
    }
  }
};
</script>

<style>
</style>