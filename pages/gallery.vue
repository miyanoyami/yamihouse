<template>
  <v-row>
    <v-col class="text-center">
      <blockquote class="blockquote">
        絵とか貼っていきたいね

        <!-- component -->
        <viewer :images="images">
          <img v-for="src in images" :key="src" :src="src" width="180px">
        </viewer>

        <footer></footer>
      </blockquote>
    </v-col>
  </v-row>
</template>

<script>
import 'viewerjs/dist/viewer.css'
import VueViewer from 'v-viewer'
import Vue from 'vue'
Vue.use(VueViewer)
export default {
  data () {
    return {
      images: [
        '/yami.jpeg',
        '/yami_full.png'
      ]
    }
  },
  methods: {
    show () {
      this.$viewerApi({
        images: this.images
      })
    }
  }
}
</script>
