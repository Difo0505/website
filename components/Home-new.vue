<template>
  <div class="workspace">
    <div class="left-half">
      <v-card class="window window-1">
        <content-card />
      </v-card>
    </div>
    <div class="right-half">
      <v-card class="window window-2">
        <video-card />
      </v-card>
      <v-card class="window window-3">
        <get-material-shell-card />
      </v-card>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.workspace {
  display: flex;
  flex-flow: row nowrap;
  align-items: stretch;
  justify-content: space-between;
  position: absolute !important;
  left: 48px;
  top: 0;
  width: 100%;
  height: 100%;;
}

.left-half {
  width: calc(50% - 48px);
  height: 100%;
}

.window-1 {
  //height: 100%;
  width: 97.5%;
  margin: auto;
  background: rgba(#191919, .85);
}

.window {
  border-radius: 0 !important;
}

.window-2 {
  background: #000;
  width: 100%;
  height: 49.5%;
  border-radius: 0 0 0 5px !important;

}

.window-3 {
  width: 100%;
  height: 49.5%;
  border-radius: 5px 0 0 0 !important;

}

.right-half {
  width: calc(50%);
  height: 100%;
  display: flex;
  flex-flow: column nowrap;
  align-items: stretch;
  justify-content: space-between;
  position: fixed;
  right: 0;
}

video-card, get-material-shell-card {
  height: 100%;
  width: 100%;
}
</style>

<style scoped>
/deep/.theme--dark.v-card.window-1 {
  background: rgba(25,25,25,.85);
}

/deep/.theme--dark.v-card.window-2 {
  background:#000;
}
</style>

<script>
import ContentCard from '~/components/Content-Card';
import VideoCard from '~/components/Video-Card';
import GetMaterialShellCard from '~/components/Get-Material-Shell-Card'


export default {
  components: {
    ContentCard,
    VideoCard,
    GetMaterialShellCard
  }
}
</script>
