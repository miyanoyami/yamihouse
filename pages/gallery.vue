<template>
  <v-row>
    <v-col class="text-center">
      <p class="text-h5">イラスト置き場</p>
      <blockquote class="blockquote">
        <viewer :images="images">
          <img v-for="src in images" :key="src" :src="src" width="180px">
        </viewer>
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
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_b.png',
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_full.png',
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_maro_20211115.png',
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_stella_20210813.jpeg',
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_ibara_20210818.jpeg',
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_arika_20210822.png',
        'https://miyanoyami-static.s3.ap-northeast-1.amazonaws.com/gallery/yami_stella_20210922.png'
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
