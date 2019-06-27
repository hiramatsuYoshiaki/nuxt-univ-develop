<template>
  <div class="host">
    <div class="flex-container">
      <div class="side-col">
        <a href="#a1">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 1}" @click="menuActive(1)">
            1. Netlifyでホスティングする。
          </p>
        </a>
        <a href="#a2">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 2}" @click="menuActive(2)">
            2. Firebaseyでホスティングする。
          </p>
        </a>
        <a href="#a3">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 3}" @click="menuActive(3)">
            3. Herokuでホスティングする。
          </p>
        </a>
        <a href="#a4">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 4}" @click="menuActive(3)">
            4. GitHub Pagesでホスティングする。
          </p>
        </a>
      </div>

      <div class="main-col">
        <div id="a1" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            1. Netlifyでホスティングする。
          </div>
          <!-- <div class="mainTitle">
            <div class="h3-res">
              GitHubリポジトリをcloneしてローカルプロジェクトを作る
            </div>
          </div> -->
          <div class="mainDescription">
            <p>Netlifyでホスティングする設定</p>
          </div>
          <div class="mainOperation">
            1. Netlifyにログインする。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd11)" />
            </div>
          </div> -->
          <div class="mainOperation">
            2. 画面右上の「New site from Git」を押すとリポジトリ選択画面に移動する。
            Githubボタンを押します。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd12)" />
            </div>
          </div> -->
          <div class="mainOperation">
            3. リポジトリを選択
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd13)" />
            </div>
          </div>
          <div class="mainOperation">
            4. リポジトリ内でデプロイの対象となるブランチを指定します。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd14)" />
            </div>
          </div>
          <div class="mainOperation">
            5. ビルドの設定をします。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd15)" />
            </div>
          </div>
          <div class="mainOperation">
            6. Deploy site」のボタンを押してしばらく待ちましょう。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd16)" />
            </div>
          </div>
        </div>

        <div id="a2" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            2. Firebaseyでホスティングする。
          </div>
          <!-- <div class="mainTitle">
            <div class="h3-res">
              新規プロジェクト用のリポジトリを作り、チーム開発のバージョン管理を行います。
            </div>
          </div> -->
          <div class="mainDescription">
            <p>Firebaseで新規プロジェクトを作成しディプロイする。</p>
          </div>
          <div class="mainOperation">
            1. Firebaseで新規プロジェクトを作成する。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd21)" />
            </div>
          </div> -->

          <div class="mainOperation">
            2. Firebase CLI をインストール
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd22)" />
            </div>
          </div>
          <div class="mainOperation">
            3. Firebase プロジェクトにアクセスする
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd23)" />
            </div>
          </div>
          <div class="mainOperation">
            4. サイトを初期化する（firebasercとfirebase.jsonを作る）
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd24)" />
            </div>
          </div>
          <div class="mainOperation">
            5. アプリケーションのルートディレクトリにfirebasercとfirebase.jsonができていることを確認する。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd25)" />
            </div>
          </div> -->
          <div class="mainOperation">
            6. buildもしくは、generateする
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd26)" />
            </div>
          </div>
          <div class="mainOperation">
            7. ローカルで実行してテストしてみる
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd27)" />
            </div>
          </div>
          <div class="mainOperation">
            8. firebaseにディプロイする
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd28)" />
            </div>
          </div>
          <div class="mainOperation">
            9. firebaseにホスティングされていることを確認する。
            https://nuxt-app-xxxx.firebaseapp.com/にアクセスするか、firebaseのダッシュボードからアクセスして確認する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd29)" />
            </div>
          </div>
        </div>

        <div id="a3" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            3. Herokuでホスティングする。
          </div>
          <!-- <div class="mainTitle">
            <div class="h3-res">
              GitHubリポジトリをcloneしてローカルプロジェクトを作る
            </div>
          </div> -->
          <div class="mainDescription">
            <p>プロジェクト内でのHerokuのディプロイ設定</p>
          </div>
          <div class="mainOperation">
            1. package.json 内の heroku-postbuild スクリプトを使って、Heroku に npm run build を実行するよう伝えます。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd31)" />
            </div>
          </div>
          <div class="mainOperation">
            2. プロジェクトのルートに Procfile (ファイル拡張子を付けずにファイル名を Procfile という名前にします）を新規作成します。以下の行を記入します。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd32)" />
            </div>
          </div>
          <br>
          <div class="mainDescription">
            <p>Herokuでホスティング設定をする。</p>
          </div>
          <div class="mainOperation">
            1. Herokuにログインし、画面ミグ上の「New」ボタンから「Create new app」をクリックしてする。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd11)" />
            </div>
          </div> -->
          <div class="mainOperation">
            2. app name アプリケーション名（nuxt-univ-app2）を入力して、「create app」ボタンを押して新規プロジェクトを作成する。
          </div>

          <div class="mainOperation">
            3. Deployment methodのGitHubボタンをクリックし、Connect to GitHubのSearch for a repository to connect toにリポジトリを入力する。
          </div>

          <div class="mainOperation">
            4. 「connect」ボタンを押す。
          </div>

          <div class="mainOperation">
            5. メニューの「setting」を押す。
          </div>

          <div class="mainOperation">
            6. Config Varsの「Reveal Config Vars」を押し、key項目を追加する。
          </div>
          <div class="mainOperation">
            7. key: HOST value: 0.0.0.0を入力し、「add」ボタンを押す。
          </div>
          <div class="mainOperation">
            8. key: NPM_CONFIG_PRODUCTION value: falseを入力し、「add」ボタンを押す。
          </div>
          <div class="mainOperation">
            9. key: NODE_EVN value: productionを入力し、「add」ボタンを押す。
          </div>
          <div class="mainOperation">
            10. メニューのDeployを押す。
          </div>
          <!-- <div class="mainOperation">
            11. Add this app to a pipline項目のchoose a pipelineを押し「create new pipeline」を押す。
          </div>
          <div class="mainOperation">
            12. Name the pipelineにnuxt-univ-app2の名前を入力し、Choose a stage to add this app toの項目「staging」を選択し、「create pipeline」を押す。
          </div>
          <div class="mainOperation">
            13. productionの「add app」ボタンを押し、「Create new app」ボタンを押す。
          </div>
          <div class="mainOperation">
            14. App nameに名前を入力して、「create app」ボタンを押す。
          </div> -->
        </div>

        <div id="a4" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            4. GitHub Pagesでホスティングする。
          </div>
          <!-- <div class="mainTitle">
            <div class="h3-res">
              GitHubリポジトリをcloneしてローカルプロジェクトを作る
            </div>
          </div> -->
          <div class="mainDescription">
            <p>GitHub Pagesでホスティングする設定</p>
          </div>
          <div class="mainOperation">
            1. nuxt.config.jsを編集する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd41)" />
            </div>
          </div>
          <div class="mainOperation">
            2. コマンドラインでデプロイする。push-dir package をインストールする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd42)" />
            </div>
          </div>
          <div class="mainOperation">
            3. deploy コマンドを package.json に追加する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd43)" />
            </div>
          </div>
          <div class="mainOperation">
            4. 静的なアプリケーションを生成
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd44)" />
            </div>
          </div>
          <div class="mainOperation">
            5. デプロイする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd45)" />
            </div>
          </div>
          <div class="mainOperation">
            6. GitHubのsettignからGitHub Pagesのsouceをgh-page branchに変更する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd46)" />
            </div>
          </div>
          <div class="mainOperation">
            7. GitHub Pagesを確認する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd47)" />
            </div>
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
      $ git clone https://github.com/hiramatsuYoshiaki/nuxt-univ-app1.git
       `,
      cmd12: `
      $ npm install
      `,
      cmd13: `
      GitHubボタンを押す。
      `,
      cmd14: `
      nuxt-univ-app1
      `,
      cmd15: `
      deploy comand: nuxt generate 
      publish directory: dist
      `,
      cmd16: `
      diploy siteボタンを押す      `,
      cmd21: `
      cmd21
      `,
      cmd22: `
      $ npm install -g firebase-tools
      `,
      cmd23: `
      $ firebase login
      `,
      cmd24: `
      $ firebase init
             
      Are you ready to proceed?
      ⇒ yを押して、enterを押す
       
      ? Which Firebase CLI features do you want to set up for this folder?
      Press Space to select features, then Enter to confirm your choices.
      Hosting: Configure and deploy Firebase Hosting sites
      下矢印キーを押してリストを選択   
      ⇒ hostingを選択し、スペースキーを押して、enterを押す。(ホスティングのみ選択)
      
      ? Select a default Firebase project for this directory:
      下矢印キーを押してリストを選択（プロジェクト数が多い場合は下に隠れている） 
      ⇒ スペースキーを押してプロジェクトを選択して。enterを押す
      
      ? What do you want to use as your public directory?
      ⇒ distを入力し、enterを押す
      
      ? Configure as a single-page app (rewrite all urls to /index.html)?
      ⇒ nを入力し、enterを押す。（シングルページアプリケーションの場合はy）
       
      ? File dist/index.html already exists. Overwrite?
      ⇒ ｎを入力し、enterを押す
     `,
      cmd25: `
      cmd25
      `,
      cmd26: `
      $ npm run build もしくは、npm run generate
      `,
      cmd27: `
      $ firebase serve
      localhost:5000/にアクセスして確認する
      `,
      cmd28: `
      $ firebase deploy
      `,
      cmd29: `
      https://nuxt-app-xxxx.firebaseapp.com/にアクセス
      `,
      cmd31: `
      "scripts": {
      "dev": "nuxt",
      "build": "nuxt build",
      "start": "nuxt start",
      "heroku-postbuild": "npm run build"
      }
      `,
      cmd32: `
      web: nuxt start
      `,
      cmd41: `
      export default {
         router: {
           base: '/<repository-name>/' 
         }
      }
      `,
      cmd42: `
      $ npm install push-dir --save-dev
      `,
      cmd43: `
      "scripts": {
         "dev": "nuxt", 
         "build": "nuxt build", 
         "start": "nuxt start", 
         "generate": "nuxt generate", 
         "deploy": "push-dir --dir=dist --branch=gh-pages --cleanup" },
      `,
      cmd44: `
      $ npm run generate
      `,
      cmd45: `
      $ npm run deploy
      `,
      cmd46: `
      gh-page branch
      `,
      cmd47: `
      https://hiramatsuyoshiaki.github.io/nuxt-create-app1/
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
.host{
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
