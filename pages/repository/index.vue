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
    <transition name="mainCon" appear>
      <div class="content-main">
        <ConRepository />
      </div>
    </transition>
    <transition name="mainCon" appear>
      <div class="content-footer">
        <ContentFooter />
      </div>
    </transition>

    <transition appear name="transitionScreen">
      <TransitionScreen v-if="page === '/repository'" />
    </transition>
  </div>
</template>
<script>
import TransitionScreen from '~/components/transition/TransitionScreen.vue'
import ConRepository from '~/components/content/repository/ConRepository.vue'

import ConHeader from '~/components/content/ConHeader.vue'
import ContentFooter from '~/components/content/ContentFooter.vue'

export default {
  layout: 'topPage',
  components: {
    TransitionScreen,
    ConRepository,
    ConHeader,
    ContentFooter
  },
  data() {
    return {
      img: require('~/assets/img/fuji1.jpg'),
      pageTitle: 'Repository ',
      pageSubTitle: 'Step1',
      pageDiscription: 'プロジェクト作成',
      pageDiscriptionDetail: 'GitHubからCloneしてローカルにプロジェクトを作成します。'
    }
  },
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
  },
  computed: {
    page() {
      return this.$store.state.page
    }
  }

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
</style>
