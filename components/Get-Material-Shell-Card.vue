<template>
  <main>
    <h2 class="card-title">Get Material Shell</h2>
    <v-btn class="download-button" :key="data.name" v-for="data in downloadButtonData" :href="data.link" :alt="data.name" :title="data.name">
        <span v-text="data.text"></span>
        <v-icon class="download-button-icon">{{data.icon}}</v-icon>
    </v-btn>
  </main>
</template>

<style lang="scss" scoped>
main {
  background: #191919;
  opacity: .7;
  height: 100%;
  width: 100%;
  padding: 1rem;
}

.download-button {
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: space-between;
  width: fit-content;
  padding: 1.5rem !important;
  margin: 1.25rem !important;
  margin-left: 0 !important;
  margin-top: .75rem !important;
}

.download-button-icon {
    margin-left: 1rem;
}

.card-title {
    font-weight: 300;
    font-size: 2rem;
    margin-bottom: 0 !important;
}
</style>


<script lang="ts">
export default {
    data(){
        return {
            downloadButtonData: [
                {
                    name: "Gnome Extensions",
                    text: "Go to the Gnome extensions website",
                    icon: "mdi-puzzle",
                    link: "https://extensions.gnome.org/"
                },
                {
                    name: "Github",
                    text: "View on Github",
                    icon: "mdi-github",
                    link: "https://github.com/PapyElGringo/material-shell/"
                },
                {
                    name: "Download source",
                    text: "Download source code",
                    icon: "mdi-file-download",
                    link: "https://github.com/PapyElGringo/material-shell/"
                }
            ]
        }
    }
}
</script>
