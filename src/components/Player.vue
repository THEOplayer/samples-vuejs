<template>
  <div class="theoplayer-container video-js theoplayer-skin" ref="theoplayer"></div>
</template>

<script>
export default {
  props: ["source"],
  mounted: function() {
    this.playerInit();
  },
  methods: {
    playerInit() {
      const player = new window.THEOplayer.Player(this.$refs.theoplayer, {
        fluid: true,
        libraryLocation: "./libs/THEOplayer"
      });
      player.source = {
        sources: this.source
      };
    }
  }
};
</script>