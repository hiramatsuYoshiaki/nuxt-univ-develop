<template>
  <div class="project">
    <div class="flex-container">
      <div class="side-col">
        <a href="#a1">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 1}" @click="menuActive(1)">
            1. Netlify
          </p>
        </a>
        <a href="#a2">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 2}" @click="menuActive(2)">
            2. Heroku
          </p>
        </a>
        <a href="#a3">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 3}" @click="menuActive(3)">
            3. Google Firebase
          </p>
        </a>
        <a href="#a4">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 4}" @click="menuActive(4)">
            4. Google Cloud Platform
          </p>
        </a>
        <a href="#a5">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 5}" @click="menuActive(5)">
            5. GitHub Pages
          </p>
        </a>
      </div>

      <div class="main-col">
        <div id="a1" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            1. Netlify ディプロイ
          </div>
          <div class="flex-card-container ">
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivApp1 + ') center / cover no-repeat'}"
              />

              <div class="card-primary-title">
                nuxt-nuxt-app1
              </div>
              <div class="card-primary-sub-title">
                NuxtアプリケーションをNetlifyへホスティング
              </div>
              <div class="card-detail">
                <!-- <div class="card-supporting-title">
                  GitHub Repository
                </div>
                <div class="card-supporting-title">
                  NuxtアプリケーションをGitHub Pagesへホスティング
                </div> -->
                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://nuxt-univ-app1.netlify.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-app1" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-app1/projects/1" target="_blank">
                    <button class="btn">
                      GitHub Project
                    </button>
                  </a>
                  <a href="https://www.netlify.com/" target="_blank">
                    <button class="btn">
                      Netlify
                    </button>
                  </a>
                </div>
              </div>
              <!-- <div class="card-action  ">
                <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                  <button class="btn">
                    Demo Page
                  </button>
                </a>
              </div> -->
            </div>
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivDevelop + ') center / cover no-repeat'}"
              />

              <div class="card-primary-title">
                nuxt-nuxt-develop
              </div>
              <div class="card-primary-sub-title">
                Nuxtのホスティングデモ
              </div>
              <div class="card-detail">
                <!-- <div class="card-supporting-title">
                  GitHub Repository
                </div>
                <div class="card-supporting-title">
                  NuxtアプリケーションをGitHub Pagesへホスティング
                </div> -->
                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://optimistic-poitras-8394df.netlify.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-develop/pull/1" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>

                  <a href="https://www.netlify.com/" target="_blank">
                    <button class="btn">
                      Netlify
                    </button>
                  </a>
                </div>
              </div>
              <!-- <div class="card-action  ">
                <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                  <button class="btn">
                    Demo Page
                  </button>
                </a>
              </div> -->
            </div>
            <div class="card-container" />
          </div>
        </div>

        <div id="a2" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            2. Heroku ディプロイ
          </div>
          <div class="flex-card-container ">
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivApp2Heroku + ') center / cover no-repeat'}"
              />

              <div class="card-primary-title">
                nuxt-univ-app2-heroku
              </div>
              <div class="card-primary-sub-title">
                NuxtアプリケーションをHerokuへホスティング
              </div>
              <div class="card-detail">
                <!-- <div class="card-supporting-title">
                  GitHub Repository
                </div>
                <div class="card-supporting-title">
                  NuxtアプリケーションをGitHub Pagesへホスティング
                </div> -->
                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://nuxt-univ-app2-prod.herokuapp.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-app2-heroku" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                  <a href="https://jp.heroku.com/" target="_blank">
                    <button class="btn">
                      Heroku
                    </button>
                  </a>
                </div>
              </div>
              <!-- <div class="card-action  ">
                <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                  <button class="btn">
                    Demo Page
                  </button>
                </a>
              </div> -->
            </div>
            <div class="card-container" />
            <div class="card-container" />
          </div>
        </div>
        <div id="a3" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            3. Firebase ディプロイ
          </div>
          <div class="flex-card-container ">
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivFirebaseHosting + ') center / cover no-repeat'}"
              />

              <div class="card-primary-title">
                nuxt-univ-firebase-hosting
              </div>
              <div class="card-primary-sub-title">
                NuxtアプリケーションをFirebaseへホスティング
              </div>
              <div class="card-detail">
                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://nuxt-app2.firebaseapp.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-firebase-hosting" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                  <a href="https://circleci.com/" target="_blank">
                    <button class="btn">
                      Circl CI
                    </button>
                  </a>
                  <a href="https://firebase.google.com/?hl=ja" target="_blank">
                    <button class="btn">
                      Firebase
                    </button>
                  </a>
                </div>
              </div>
            </div>
            <!-- <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivFirebaseApp2 + ') center / cover no-repeat'}"
              />

              <div class="card-primary-title">
                nuxt-univ-firebase-app2
              </div>
              <div class="card-primary-sub-title">
                NuxtアプリケーションをFirebaseへホスティング
              </div>
              <div class="card-detail">

                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://nuxt-app-6f771.firebaseapp.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-firebase-app2" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                  <a href="https://circleci.com/" target="_blank">
                    <button class="btn">
                      Circl CI
                    </button>
                  </a>
                  <a href="https://firebase.google.com/?hl=ja" target="_blank">
                    <button class="btn">
                      Firebase
                    </button>
                  </a>
                </div>
              </div>

            </div> -->
            <div class="card-container" />
            <div class="card-container" />
          </div>
        </div>
        <div id="a4" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            4. Google Cloud Platform ディプロイ
          </div>
          <div class="flex-card-container ">
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivCreateGaeHosting + ') center / cover no-repeat'}"
              />
              <div class="card-primary-title">
                nuxt-univ-create-gae-hosting
              </div>
              <div class="card-primary-sub-title">
                Nuxtアプリケーションを GoogleCloudPlatform(GAE) へホスティング
              </div>
              <div class="card-detail">
                <!-- <div class="card-supporting-title">
                  GitHub Repository
                </div>
                <div class="card-supporting-title">
                  NuxtアプリケーションをGitHub Pagesへホスティング
                </div> -->

                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://nuxt-univ-gae-app.appspot.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-create-gae-hosting" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                  <a href="https://cloud.google.com/solutions/websites/?hl=ja" target="_blank">
                    <button class="btn">
                      Google Cloud Platform
                    </button>
                  </a>
                </div>
              </div>
              <!-- <div class="card-action  ">
                <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                  <button class="btn">
                    Demo Page
                  </button>
                </a>
              </div> -->
            </div>
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtUnivGaeTodo2 + ') center / cover no-repeat'}"
              />
              <div class="card-primary-title">
                nuxt-univ-create-gae-todo2
              </div>
              <div class="card-primary-sub-title">
                Nuxtアプリケーションを GoogleCloudPlatform(GAE) へホスティング
              </div>
              <div class="card-detail">
                <!-- <div class="card-supporting-title">
                  GitHub Repository
                </div>
                <div class="card-supporting-title">
                  NuxtアプリケーションをGitHub Pagesへホスティング
                </div> -->

                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://nuxt-univ-create-gae-todo.appspot.com/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-univ-create-gae-todo2" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                  <a href="https://cloud.google.com/solutions/websites/?hl=ja" target="_blank">
                    <button class="btn">
                      Google Cloud Platform
                    </button>
                  </a>
                </div>
              </div>
              <!-- <div class="card-action  ">
                <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                  <button class="btn">
                    Demo Page
                  </button>
                </a>
              </div> -->
            </div>
            <div class="card-container" />
          </div>
        </div>
        <div id="a5" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            5. GitHub Pages ディプロイ
          </div>
          <div class="flex-card-container ">
            <div class="card-container card-container-border">
              <div
                class="card-rich-Media "
                :style="{'background':'url(' + nuxtCreateApp1 + ') center / cover no-repeat'}"
              />
              <div class="card-primary-title">
                nuxt-create-app1
              </div>
              <div class="card-primary-sub-title">
                NuxtアプリケーションをGitHub Pagesへホスティング
              </div>
              <div class="card-detail">
                <!-- <div class="card-supporting-title">
                  GitHub Repository
                </div>
                <div class="card-supporting-title">
                  NuxtアプリケーションをGitHub Pagesへホスティング
                </div> -->

                <div class="card-action-title">
                  Trial Product
                </div>
                <div class="card-tag">
                  <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                    <button class="btn">
                      Demo Page
                    </button>
                  </a>
                  <a href="https://github.com/hiramatsuYoshiaki/nuxt-create-app1" target="_blank">
                    <button class="btn">
                      GitHub Repository
                    </button>
                  </a>
                </div>
              </div>
              <!-- <div class="card-action  ">
                <a href="https://hiramatsuyoshiaki.github.io/nuxt-create-app1/" target="_blank">
                  <button class="btn">
                    Demo Page
                  </button>
                </a>
              </div> -->
            </div>
            <div class="card-container" />
            <div class="card-container" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

// import readMe from '~/assets/readMe/readMe.md'
// import TransitionScreen from '~/components/transition/TransitionScreen.vue'

//       img: require('~/assets/img/img3668.jpg'),
export default {
  data() {
    return {
      nuxtCreateApp1: require('~/assets/img/capcher/nuxtCreateApp1.gif'),
      nuxtUnivApp1: require('~/assets/img/capcher/nuxt-univ-app1.gif'),
      nuxtUnivDevelop: require('~/assets/img/capcher/nuxt-univ-develop.gif'),
      nuxtUnivApp2Heroku: require('~/assets/img/capcher/nuxt-univ-app2-heroku.gif'),
      nuxtUnivFirebaseApp2: require('~/assets/img/capcher/nuxt-univ-firebase-app2.gif'),
      nuxtUnivFirebaseHosting: require('~/assets/img/capcher/nuxt-univ-firebase-hosting.gif'),
      nuxtUnivCreateGaeHosting: require('~/assets/img/capcher/nuxt-univ-create-gae-hosting.gif'),
      nuxtUnivGaeTodo2: require('~/assets/img/capcher/nuxt-univ-gae-todo2.gif'),
      cardImg: require('~/assets/img/fuji1.jpg'),
      selectMenu: -1,
      cmd11: ` 
      $ git clone https://github.com/hiramatsuYoshiaki/nuxt-univ-app1.git
       `,
      cmd12: `
      $ npm install
      `,
      cmd13: `
      $ npm run dev
      `,
      cmd14: `
      http://localhost:3000/で確認する。
      `,
      cmd21: `
      NEW」または、「Start a project」ボタンを押す。
      `,
      cmd22: `
      Repository name: リポジトリ名
      Description: 簡単な説明
      publicにチェックを入れる
      Initialize this repository with a READMEはチェックせず画面下のほうにある 「Create repository」 ボタンをクリックします。
      `,
      cmd23: `
      git add .
      git commit -m "first commit"
      git remote add origin https://github.com/リポジトリ名/プロジェクト名
      git push -u origin master
      `
    }
  },
  //   props: {
  //     pageTitle: {
  //       type: String,
  //       default: 'a'
  //     },
  //   }

  //   computed: {
  // page() {
  //   return this.$store.state.page
  // }

  // readMe() {
  //   return readMe
  // }

  //   },
  methods: {
    menuActive(index) {
      this.selectMenu = index
    }
  }
//   created: function () {
//     this.isMenu = false
//   }
//   methods: {
//     link_commit(linkPath) {
//       this.active = true
//       this.$store.commit('pagePathSet', linkPath)
//       setTimeout(() => {
//         this.$router.push({ path: linkPath })
//       }, 500)
//     }
//   }
}
</script>
<style scoped lang="scss">
.project{
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 2rem 2rem;
  @media (min-width: 768px) {
      padding: 8rem 8rem;
  };
  border: 1px solid  rgba(0,0,0,.2);
}
.flex-container{
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  @media (min-width: 992px) {
    flex-direction: row;
  };
}
.side-col{
  // background-color: rgb(187, 248, 187);
    width: 100%;
    display: none;
    @media (min-width: 992px) {
        width: 30%;
        display: block;
        padding-right: 10rem;
    };
    // padding-right: 8rem;
    // padding-bottom: 2rem;
    padding: 2rem;
    section{
      margin-bottom: 2rem;
    }
    // h3{
    //   color:#000000;
    //   font-weight: 600;
    // }
    p{
      color:rgb(70, 69, 69);
    }
    // border: 1px solid  rgba(0,0,0,.2);

}
.main-col{
    width: 100%;
    @media (min-width: 992px) {
        width: 70%;
        padding-right: 10rem;
        padding: 2rem;
    };
    section{
      margin-bottom: 2rem;
    }
    // p{
    //   color:rgb(70, 69, 69);
    // }
    // background-color: rgb(245, 165, 165);

}
// .card3-col{
//   border:1px solid black;
//     width: 100%;
//     height: 100%;
//     padding: 2.4rem;
//     @media (min-width: 992px) {
//         width: 33.333%;
//     };
// }

.main-wrap{
    margin-top: 3rem;
}
.topMenu{
    color:rgb(70, 69, 69);
    font-weight: 500;
    cursor: pointer;
    padding:0.5rem ;
}
.activeTopMenu{
    background-color: lightgreen;
    border-radius: 2px;
}
.subMenu{
    padding-left: 1.5rem;
}

.topMain{
    border-bottom: 1px solid green;
    margin: 6rem 2rem 2rem 0;

}
.mainTitle{
    margin: 2rem 2rem 2rem 2rem;
    @media (min-width: 992px) {
        margin: 6rem 2rem 2rem 2rem;
    };

}
.mainDescription{
    p{
        font-weight: 700;
    }
    margin: 2rem 2rem 2rem 2rem;
}
.mainOperation{
    // p{
    //     color: gray;
    // }
    margin: 2rem 2rem 2rem 2rem;
    a{
      color: blue
    }
}
.mainComandWrap{
    background-color: rgb(150, 159, 165);
    padding: 1rem;
    border-radius: 2px;
    // font-size: 1rem;
}
.mainComand{
    font-size: 1.6rem;
    line-height: 2.5rem;
}
.h1-res{
    color: rgb(5, 121, 5);
    font-weight:700;
    font-size: 2rem;
    @media (min-width: 992px) {
        font-size: 4rem;
    };
}
.h3-res{
    color: rgb(53, 53, 53);
    font-weight:700;
    font-size: 2rem;
    @media (min-width: 992px) {
        font-size: 4rem;
    };
}
p{
    color:rgb(70, 69, 69);
}
.card-primary-title{
  color: rgb(5, 121, 5);
    font-weight:700;
    font-size: 1.4rem;
    @media (min-width: 992px) {
        font-size: 2rem;
    };
}

</style>
