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
            "//cdn.theoplayer.com/video/elephants-dream/playlist.m3u8"
        }
      ]
    };
  }
};
</script>

