<template>
  <div class="container">
    <div
      class="content-header"
      :style="{ 'background-image': 'url(' + dockerBg3 + ')' }"
    >
      <div class="content con-wraper">
        <div class="con-hed-logo">
          <logo />
        </div>
        <div class="con-hed-title">
          <h1 class="title">
            h-works
          </h1>
          <h2 class="subtitle">
            Nuxt.js Universal
          </h2>
          <h2 class="subtitle">
            GitHub + Auto Deploy
          </h2>
          <div class="top-project">
            <nuxt-link to="/project">
              <p class="subtitle">
                Demo Project
              </p>
            </nuxt-link>

            <h3>Netlify</h3>
            <h3>Heroku</h3>
            <h3>Google Firebase</h3>
            <h3>Google Cloud Platform</h3>
            <h3>GitHubPage</h3>
          </div>
        </div>
      </div>
    </div>
    <div class="content-header-second con-wraper">
      <p>Nuxt Starter Template</p>
      <p>nuxt create </p>
    </div>
    <h3>Setting </h3>
    <transition name="mainCon" appear>
      <div class="content-main-tec" :style="{ 'background-image': 'url(' + dockerBgRs1 + ')' }">
        <div class="content con-wraper con-mein-top">
          <section class="con-main-sec">
            <h5>REPOSITORY</h5>
            <h2>プロジェクト作成</h2>
            <div class="con-main-line" />
            <div class="con-main-list">
              <p>GitHubからCloneしてローカルにプロジェクトを作成します。</p>
            </div>
            <div class="page-link" @click="link_commit('/project')">
              詳細
            </div>
          </section>
          <section class="con-main-sec">
            <h5>CONFIGU</h5>
            <h2>初期設定</h2>
            <div class="con-main-line" />
            <div class="con-main-list">
              <p>Nuxt.configの初期設定を行い、アプリ開発の準備を行います。</p>
            </div>
            <div class="page-link" @click="link_commit('/config')">
              詳細
            </div>
          </section>
          <section class="con-main-sec">
            <h5>HOST</h5>
            <h2>ホスティング</h2>
            <div class="con-main-line" />
            <div class="con-main-list">
              <!-- <p>
                Firebaseのプロジェクトを作成し、ホスティングする準備をします。また、Realtime Database,
                Storage,Authenticationなども設定します。
              </p> -->
              <p>
                ホスティングの設定をします。
              </p>
            </div>
            <div class="page-link" @click="link_commit('/host')">
              詳細
            </div>
          </section>
          <section class="con-main-sec">
            <h5>AUTO-DEPLOY</h5>
            <h2>自動ディプロイ</h2>
            <div class="con-main-line" />
            <div class="con-main-list">
              <p>ホストへ自動ディプロイする設定を作ります。</p>
            </div>
            <div class="page-link" @click="link_commit('/deploy')">
              詳細
            </div>
          </section>
        </div>
      </div>
    </transition>

    <transition name="mainCon" appear>
      <div class="content-footer">
        <ContentFooter />
      </div>
    </transition>

    <transition appear name="transitionScreen">
      <TransitionScreen v-if="page === '/'" />
    </transition>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import TransitionScreen from '~/components/transition/TransitionScreen.vue'
import ContentFooter from '~/components/content/ContentFooter.vue'

export default {
  layout: 'topPage',
  components: {
    Logo,
    ContentFooter,
    TransitionScreen
  },
  data() {
    return {
      img: require('~/assets/img/img1578.jpg'),
      dockerBg: require('~/assets/img/docker.svg'),
      dockerBg3: require('~/assets/img/docker3.svg'),
      dockerBgRs1: require('~/assets/img/dockerRevers1.svg'),

      pageTitle: 'Landing Content',
      pageSubTitle: 'Nuxt.js Demo Site',
      pageDiscription: 'Landing',
      pageDiscriptionDetail: 'Vue.jsのフレームワークNuxt.jsを使ったデモサイトです。'
    }
  },
  head() {
    return {
      title: this.pageTitle,
      meta: [
        { hid: 'description',
          name: 'landing by Nuxt.js',
          content: 'このページは、Vue.jsフレームワークのNuxt.jsを使って作成したデモサイトです。' }
      ]
    }
  },
  computed: {
    page() {
      return this.$store.state.page
    }
  },
  methods: {
    link_commit(linkPath) {
      this.active = true
      this.$store.commit('pagePathSet', linkPath)
      setTimeout(() => {
        this.$router.push({ path: linkPath })
      }, 500)
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
//content base-----------------------
.container{
  margin-top: $header-height;
  width: 100vw;
  @extend %center;
  flex-direction: column;
  margin:0;
  padding: 0;
}
.content{
  width: 100%;
  display:flex;
  flex-direction: column;
  @media(min-width: 992px){
    display:flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
  }
}
// wraper-----------------------------
.con-wraper{
  padding: 8rem 2rem;
  @media(min-width: 992px){
    padding: 15rem 5rem;
  }
}
//header-----------------------------
.content-header{
  width: 100vw;
  height: 100vh;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
.con-hed-logo{
  @extend %center;
  width:100%;
  @media(min-width: 992px){
    width:40%;
  }
}
.con-hed-title{
  display:flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  @media(min-width: 992px){
       justify-content: flex-start;
    align-items: flex-start;
  }
  .top-project{
    margin-top: 2rem;
    a{
      cursor:pointer;
      :hover{
        color: green;
      }
    }
    .subtitle{
      border: solid 1px #fff;
      display: block;
      padding: .5rem;
      margin: 1rem 0;
    }
  }
  h1{
    font-size: 3.0rem;
    font-weight: 700;
    line-height: 3.5rem;
  }
  h2{
    font-size: 2rem;
    font-weight: 500;
    line-height: 2.5rem;
  }
  .sign-in-text{
    font-size: 1.6rem;
    font-weight: 500;
    line-height: 2.1rem;
  }
  @media(min-width: 992px){
    width:70%;
    h1{
      font-size: 8.0rem;
      font-weight: 700;
      line-height: 8.5rem;
    }
    h2{
      font-size: 4.0rem;
      font-weight: 400;
      line-height: 4.5rem;
    }
    .sign-in-text{
    font-size: 2.0rem;
      font-weight: 500;
      line-height: 2.5rem;
   }
  }
  .btn-box{
    width: 30rem;
    margin-top: 2rem;
    padding:1rem 3rem;
    border: 2px solid #fff;
    border-radius: 5px;
    cursor: pointer;
    display:flex;
    justify-content: center;
    align-items: center;
    @media(min-width: 992px){
      justify-content: flex-start;
      align-items: flex-start;
    }
  }
  .image-mask{
    border-radius: 50%;
    width:5rem;
    height:5rem;
  }
}

// content-header-second-------------------------
.content-header-second{
  @extend %center;
  flex-direction: column;
  width: 100%;
}
// content-main-title----------------------------
.content-main-tec{
  width: 100vw;
  height: 100%;
  @media(min-width: 992px){
    height: 100vh;
  }
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
.con-mein-top{
  justify-content:space-between;
  align-items: stretch;
}
.con-main-sec{
  position: relative;
  width:100%;
  padding: 2rem 2rem 6rem 2rem;
  margin-bottom: 2rem;
  @media(min-width: 992px){
    width:20%;
  }
  background-color: #fff;
  color: #212121;
  border: 2px solid rgba(0,0,0,.3);
  border-radius: 5px;
  h5{
    color: #696969;
    font-weight: 300;
  }

}
.con-main-sec{
  h1{
    font-size: 3.0rem;
    font-weight: 700;
    line-height: 3.5rem;
  }
  h2{
    font-size: 2rem;
    font-weight: 500;
    line-height: 2.5rem;
  }
  p{
    font-size: 1.2rem;
    font-weight: 500;
    line-height: 1.4rem;
  }
  @media(min-width: 992px){
    h1{
      font-size: 6.0rem;
      font-weight: 700;
      line-height: 6.5rem;
    }
    h2{
      font-size: 4.0rem;
      font-weight: 400;
      line-height: 4.5rem;
    }
    p{
      font-size: 2rem;
      font-weight: 400;
      line-height: 2.5rem;
    }
  }
}
.con-main-line{
  width: 100%;
  height: 1px;
  background-color: #212121;
  margin: 2rem 0;
}
.page-link{
  position: absolute;
  bottom: 0;
  right: 0;
  text-align: right;
  color: rgb(6, 140, 250);
  font-weight: 700;
  width: 100%;
  cursor: pointer;
  display:block;
  margin: 2rem;
}
// main inpliment------------------------------
.content-main-implement{
  width: 100vw;
  background-color: rgb(230,230,230);
  color: #212121;
  border-top: rega(0,0,0,.2);
}
.content-main-title{
  @extend %center;
  flex-direction: column;
  width: 100%;
  padding: 5rem 0 0 0 ;
}
.con-mein-project{
  justify-content:space-between;
}
.con-main-imp{
  width:100%;
  padding: 2rem;
  background-color: rgb(170, 170, 170);
  @media(min-width: 992px){
    width:30%;
  }
  border-radius: 5px;
  margin-bottom: 2rem;
}
.con-main-impList{
  padding: 2rem;
  background-color: rgb(230,230,230);
  margin: 2rem 0;
  border-radius: 5px;
}
.gitHub-link{
  text-align: left;
  color: #212121;
  font-weight: 700;
  width: 100%;
  cursor: pointer;
  display:block;
}

.links{
  @extend %center;
}
.links a{
  display: inline-block;
  margin: 0 2rem;
  cursor: pointer;
}
.word-wrap{
  word-wrap: break-word;
}
.title{
  margin-top:2rem;
}
.content-footer{
  width: 100vw;
  display:flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-bottom: -5rem;
}

.done {
  text-decoration: line-through;
}
</style>
