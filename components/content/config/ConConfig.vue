<template>
  <div class="config">
    <div class="flex-container">
      <div class="side-col">
        <a href="#a1">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 1}" @click="menuActive(1)">
            1. SASSを使う
          </p>
        </a>
        <a href="#a2">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 2}" @click="menuActive(2)">
            2. SASS変数を使う
          </p>
        </a>
        <a href="#a3">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 3}" @click="menuActive(3)">
            3. eslintフォーマットエラー
          </p>
        </a>
        <a href="#a4">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 4}" @click="menuActive(4)">
            4. eslintrc.js
          </p>
        </a>
        <a href="#a5">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 5}" @click="menuActive(5)">
            5. Google Serch Colsoleを使う
          </p>
        </a>
        <a href="#a6">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 6}" @click="menuActive(6)">
            6. Google Analyticsを使う
          </p>
        </a>
        <a href="#a7">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 7}" @click="menuActive(7)">
            7. サイトマップ自動生成う
          </p>
        </a>
      </div>

      <div class="main-col">
        <div id="a1" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            1. SASSを使う
          </div>
          <div class="mainDescription">
            <p>SASSを利用したい場合は node-sass および sass-loader パッケージをインストールします。</p>
          </div>
          <div class="mainOperation">
            1. node-sass sass-loaderをインストールする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd11)" />
            </div>
          </div>
          <div class="mainOperation">
            2. nuxt.configに設定を追記する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd12)" />
            </div>
          </div>
          <div class="mainOperation">
            3. component styleタグを変更する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd13)" />
            </div>
          </div>
        </div>

        <div id="a2" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            2. SASS変数を使う
          </div>
          <div class="mainDescription">
            <p>SASS変数をimportなしで利用したい場合は @nuxtjs/style-resources パッケージをインストールします。</p>
          </div>
          <div class="mainOperation">
            1. @nuxtjs/style-resourcesrをインストールする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd21)" />
            </div>
          </div>

          <div class="mainOperation">
            2. nuxt.configに設定を追記する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd22)" />
            </div>
          </div>
          <div class="mainOperation">
            3. sass変数をimportなしで使えます。例
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd23)" />
            </div>
          </div>
        </div>
        <div id="a3" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            3. eslintフォーマットエラー
          </div>
          <div class="mainDescription">
            <p>アプリを起動するたびにeslintのエラーが発生し、「--fixオプションで修正可能な可能性があります」と表示されるエラー対応。</p>
          </div>
          <div class="mainOperation">
            1. eslintrc.jsに設定追記する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd31)" />
            </div>
          </div>
        </div>
        <div id="a4" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            4. eslintrc.js
          </div>
          <div class="mainDescription">
            <p>consol.logをしようするための、eslintrc.jsの設定をする。</p>
          </div>
          <div class="mainOperation">
            1. eslintrc.js.に設定する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd41)" />
            </div>
          </div>
        </div>
        <div id="a5" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            5. Google Serch Colsoleを使う
          </div>
          <div class="mainDescription">
            <p>Google Serch Colsoleの設定を行う。</p>
          </div>
          <div class="mainOperation">
            1. Google Serch Colsoleからメタタグを取得
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd51)" />
            </div>
          </div>
          <div class="mainOperation">
            2. nuxt.config に設定をする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd52)" />
            </div>
          </div>
        </div>
        <div id="a6" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            6. Google Analyticsを使う
          </div>
          <div class="mainDescription">
            <p>Google Analyticsを使うための設定を行う。</p>
          </div>
          <div class="mainOperation">
            1. @nuxtjs/google-analyticsをインストールする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd61)" />
            </div>
          </div>
          <div class="mainOperation">
            2. nuxt.configにアナリティクスのトラッキング IDを設定する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd62)" />
            </div>
          </div>
        </div>
        <div id="a7" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            7. サイトマップ自動生成
          </div>
          <div class="mainDescription">
            <p>Nuxt.jsで静的ファイル生成時(npm run generate)にサイトマップも自動生成する。</p>
          </div>
          <div class="mainOperation">
            1. @nuxtjs/sitemapをインストールする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd71)" />
            </div>
          </div>
          <div class="mainOperation">
            2. nuxt.configに設定を追記する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd72)" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- </div> -->
</template>
<script>
// import readMe from '~/assets/readMe/readMe.md'
// import TransitionScreen from '~/components/transition/TransitionScreen.vue'

//       img: require('~/assets/img/img3668.jpg'),
export default {
//   props: {
//     pageTitle: {
//       type: String,
//       default: 'a'
//     },
//   }
//   data() {
//     return {
//       selectMenu: -1
//     },
//   },
  data() {
    return {
      selectMenu: -1,
      cmd11: ` 
      $ npm install --save-dev node-sass sass-loader
       `,
      cmd12: `
      export default {
        css: [
            // プロジェクト内の SCSS ファイル
            '@/assets/sass/styles.scss'
        ]
      }
      `,
      cmd13: `
      <style scoped lang="scss">
      </style>
      `,

      cmd21: `
      $ npm install --save-dev @nuxtjs/style-resources
      `,
      cmd22: `
      modules: [
       '@nuxtjs/style-resources',
      ],
      styleResources: {
       sass: [
        '~/assets/sass/variable.scss',
       ],
      },
      `,
      cmd23: `
      <style scoped lang="scss">
      //@import "../../../assets/scss/common/data/thema.scss";
      .container {
          color: $text-color
       }
      </style>
      `,
      cmd31: `
      extend(config, ctx) {
       if (ctx.dev && ctx.isClient) {
            config.module.rules.push({
                enforce : 'pre',
                test    : /.(js|vue)$/,
                loader  : 'eslint-loader',
                exclude : /(node_modules)/,
                options : {
                  fix : true
                }
            });
        }
      } 
      `,
      cmd41: `
      module.exports = {
        rules: {
          'no-console': process.env.NODE_ENV === 'production' ? 'error' : 'off',
          'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off'
        }
      } 
      `,
      cmd51: `
      TaWpD9i4R5GSPzJjnTc8--t-g8bbDKbfxQX-xxxxxxx
      `,
      cmd52: `
      head: {
        meta: [
          { name: "google-site-verification",
            content: "TaWpD9i4R5GSPzJjnTc8--t-g8bbDKbfxQX-e1kgio0" },
        ],
      },
      `,
      cmd61: `
      $ npm install --save @nuxtjs/google-analytics
      `,
      cmd62: `
      modules: [
        ['@nuxtjs/google-analytics', { id: 'UA-xxxxx-x' }],
        ],
      `,
      cmd71: `
      $ npm install --save @nuxtjs/sitemap 
      `,
      cmd72: `
      modules: [
        '@nuxtjs/sitemap',
      ],
      sitemap: {
        // path: '/sitemaps.xml',//Default: sitemaps.xml
        hostname: 'https://romantic-kare-6d357c.netlify.com/',
        generate: true,
        // exclude: [
        //   '/admin'
        // ],
        routes:[
        "/",
        {
            url: '/works',
            changefreq: 'daily',
            priority: 1,
            lastmodISO: '2017-06-30T13:30:00.000Z'
        },
        "/about",
        "/contact"
        ]
      },
      `
    }
  },
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
.config{
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
//   flex-direction: column;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
//   @media (min-width: 768px) {
//       flex-direction: row;
//   };
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
</style>
