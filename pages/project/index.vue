<template>
  <div class="container">
    <div class="bgImageFull">
      <transition name="bgTran" appear>
        <div
          class="bgImage"
          :style="{ 'background-image': 'url(' + img + ') ' }"
        >
          <div class="bg_filter" />
        </div>
      </transition>
    </div>
    <div class="content-header">
      <ConHeader
        :page-title="pageTitle"
        :page-sub-title="pageSubTitle"
        :page-discription="pageDiscription"
        :page-discription-detail="pageDiscriptionDetail"
      />
    </div>
    <!-- <transition name="mainCon" appear>
      <div class="content-main">
        <div class="flex-container">
          <div class="side-col">
            side col
          </div>
          <div class="main-col">
            <div id="a1" />
            <div class="main-wrap">
              <div class="topMai h1-res">
                1. Netlify へデプロイ
              </div>
              <div class="flex-card-container">
                <div class="card-container card-container-border">
                  <div
                    class="card-rich-Media "
                    :style="{'background-image':'url(' + nuxtUnivApp1 + '); background-size: cover;'}"
                  />
                  <div
                    class="card-rich-Media "
                    :style="{'background':'url(' + nuxtUnivApp1 + ') center / cover no-repeat'}"
                  />
                  <div
                    class="gb"

                    :style="{ 'background-image': 'url(' + nuxtUnivApp1 + ') ' }"
                  >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </transition> -->
    <transition name="mainCon" appear>
      <div class="content-main">
        <ConProject />
      </div>
    </transition>
    <transition name="mainCon" appear>
      <div class="content-footer">
        <ContentFooter />
      </div>
    </transition>

    <transition appear name="transitionScreen">
      <TransitionScreen v-if="page === '/project'" />
    </transition>
  </div>
</template>
<script>
import TransitionScreen from '~/components/transition/TransitionScreen.vue'
import ConProject from '~/components/content/project/ConProject.vue'

import ConHeader from '~/components/content/ConHeader.vue'
import ContentFooter from '~/components/content/ContentFooter.vue'

export default {
  layout: 'topPage',
  components: {
    TransitionScreen,
    ConProject,
    ConHeader,
    ContentFooter
  },
  data() {
    return {
      img: require('~/assets/img/img2722.jpg'),
      pageTitle: 'Project ',
      pageSubTitle: 'Demo App',
      pageDiscription: 'デモアプリケーション',
      pageDiscriptionDetail: 'Nuxtを使ったアプリケーションのデモ',
      nuxtUnivApp1: require('~/assets/img/capcher/nuxt-univ-app1.gif')
      // nuxtCreateApp1: require('~/assets/img/capcher/nuxtCreateApp1.gif'),
      // nuxtCreateApp1: require('~/assets/img/capcher/nuxtCreateApp1.gif'),
      // nuxtUnivApp2Heroku: require('~/assets/img/capcher/nuxt-univ-app2-heroku.gif'),
      // nuxtUnivFirebaseApp2: require('~/assets/img/capcher/nuxt-univ-firebase-app2.gif'),
      // cardImg: require('~/assets/img/fuji1.jpg')
    }
  },
  computed: {
    page() {
      return this.$store.state.page
    }
  },
  // async asyncData(context) {
  //     let { data } = await axios.get(`https://my-api/posts/${params.id}`)
  //   return { title: data.title }
  //   anuxtCreateApp1 : require('~/assets/img/capcher/nuxtCreateApp1.gif'),
  //   anuxtCreateApp1: require('~/assets/img/capcher/nuxtCreateApp1.gif'),
  //   anuxtUnivApp1: require('~/assets/img/capcher/nuxt-univ-app1.gif'),
  //   anuxtUnivApp2Heroku: require('~/assets/img/capcher/nuxt-univ-app2-heroku.gif'),
  //   anuxtUnivFirebaseApp2: require('~/assets/img/capcher/nuxt-univ-firebase-app2.gif'),
  //   acardImg: require('~/assets/img/fuji1.jpg')
  //   }
  //   const nuxtUnivApp1Asynca = await require('~/assets/img/capcher/nuxt-univ-app1.gif')
  //   alert('nuxtUnivApp1Asynca')
  //   return { nuxtUnivApp1Asyncb: nuxtUnivApp1Asynca }
  // },
  head() {
    return {
      title: this.pageTitle,
      meta: [
        // `hid` は一意の識別子として使用されます。 `vmid` は動作しないので使わないでください。
        { hid: 'description',
          name: 'about by Nuxt.js',
          content: 'このページは、Nuxt.jsアプリケーションのインストールと使い方と設定を紹介しています。' }
      ]
    }
  }
  // mounted() {
  //   this.init()
  // },
  // methods: {
  //   init() {
  //     alert('init')
  //     this.nuxtUnivApp1Async = this.nuxtUnivApp1Asyncb
  //   }
  // }

}
</script>
<style scoped lang="scss">
%center{
    display:flex;
    justify-content: center;
    align-items: center;
}
%left{
    display:flex;
    justify-content: flex-start;
    align-items: center;
}
%right{
    display:flex;
    justify-content: flex-end;
    align-items: center;
}
.container{
  position: relative;
  width: 100vw;
  height: 100%;
  margin-top: $header-height;
  @extend %center;
  flex-direction: column;
}
.content-header{
    width:100vw;
    height: 35vh;
}
.content-main{
  width:100vw;
  background-color: $main-contents-color;
  color: $main-contents-text;
}
.content-footer{
  width: 100vw;
  @extend %center;
  flex-direction: column;
}
.gb{
  width:100%;
    height: 19.4rem;
    overflow: hidden;
    border-bottom:1px solid $card-container-border;
}

</style>
