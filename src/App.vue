<template>
  <div id="app">
    <Player :source="source" v-if="source"/>
  </div>
</template>

<script>
import Player from "./components/Player.vue";

export default {
  name: "app",
  components: {
    Player
  },
  data: function() {
    return {
      source: [
        {
          type: "application/x-mpegurl",
          src:
            "http://cdn.theoplayer.com/video/big_buck_bunny/big_buck_bunny_metadata.m3u8"
        }
      ]
    };
  }
};
</script>

