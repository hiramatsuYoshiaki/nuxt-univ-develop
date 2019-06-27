<template>
  <div class="deploy">
    <div class="flex-container">
      <div class="side-col">
        <a href="#a1">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 1}" @click="menuActive(1)">
            1. Netlifyへホスティングする。
          </p>
        </a>
        <a href="#a2">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 2}" @click="menuActive(2)">
            2. CircleCIでホスティングする。
          </p>
        </a>
        <a href="#a3">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 3}" @click="menuActive(3)">
            3. Herokでホスティングする。
          </p>
        </a>
        <a href="#a4">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 4}" @click="menuActive(4)">
            4. GitHub Pagesでホスティングする。
          </p>
        </a>
      </div>
      <div class="main-col">
        <div id="a1" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            1. Netlifyへホスティングする。
          </div>
          <div class="mainDescription">
            <p>GitHubリポジトリのマージから、Netlifyの自動ディプロイで、ホスティングする。</p>
          </div>
          <div class="mainOperation">
            1. Netlifyログインし、画面右上の「New site from Git」を押す。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd11)" />
            </div>
          </div>
          <div class="mainOperation">
            2. 「Github」を押し、リポジトリを選択する。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd12)" />
            </div>
          </div>
          <div class="mainOperation">
            3. Create a new site画面で各項目を入力し、「Deploy site」ボタンを押す。
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
            2. CircleCIでホスティングする。(Firebase)
          </div>
          <div class="mainDescription">
            <p>Circle CI でGitHubにpushしたら自動でFirebaseへディプロイする。</p>
          </div>
          <div class="mainOperation">
            1. CircleCIへGitHubでloginする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd21)" />
            </div>
          </div>

          <div class="mainOperation">
            2. CircleCIにログイン後、画面のサイドバーから「JOBS」を選択し該当リポジトリの歯車アイコンをクリックして画面遷移
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd22)" />
            </div>
          </div> -->
          <div class="mainOperation">
            3. BUILD SETTINGSの「Environment Variables」へ遷移し環境変数を登録する。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd23)" />
            </div>
          </div> -->
          <div class="mainOperation">
            4. デプロイ用のFirebaseトークンを取得し設定する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd24)" />
            </div>
          </div>
          <div class="mainOperation">
            5. firebaseプロジェクトIDを設定する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd25)" />
            </div>
          </div>
          <div class="mainOperation">
            6. firebaseConfigを設定する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd26)" />
            </div>
          </div>
          <div class="mainOperation">
            7. CircleCIではnpm -gでのコマンド実行が出来ないため、グローバルインストールのみの場合は、pakage.jsonに追加するために、プロジェクトにインストールする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd27)" />
            </div>
          </div>
          <div class="mainOperation">
            8. CircleCIの設定ファイルを作成
            プロジェクト直下に`.circleci/config.yml`ファイルを作成します。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd28)" />
            </div>
          </div> -->
          <div class="mainOperation">
            9. .circleci/config.ymlを編集する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd29)" />
            </div>
          </div>
          <div class="mainOperation">
            10. developブランチをビルド可能な状態でpushするとジョブが実行されます。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd210)" />
            </div>
          </div> -->
          <div class="mainOperation">
            11. Circle CIのjobs画面で確認できます。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd211)" />
            </div>
          </div> -->
          <div class="mainOperation">
            12. https://nuxt-app-xxxx.firebaseapp.com/にアクセスしホスティングされていることを確認します。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd212)" />
            </div> -->
        </div>
        <div id="a3" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            3. Herokuへホスティングする。
          </div>
          <div class="mainDescription">
            <p>GitHubリポジトリのマージから、Herokuのパイプラインで自動ディプロイし、ホスティングする。</p>
          </div>
          <div class="mainOperation">
            1. Herokuにログインし、画面ミグ上の「More」ボタンから「Add to pipeline」をクリックしてする。
          </div>
          <!-- <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd11)" />
            </div>
          </div> -->
          <div class="mainOperation">
            2. Add this app to a pipline項目のchoose a pipelineを押し「create new pipeline」を押す。
          </div>

          <div class="mainOperation">
            3. Name the pipelineに名前（nuxt-univ-app2）を入力し、Choose a stage to add this app toの項目「staging」を選択し、「create pipeline」を押す。（ステージング用のパイプライン作成）
          </div>
          <div class="mainOperation">
            4. productionの「add app」ボタンを押し、「Create new app」ボタンを押す。
          </div>
          <div class="mainOperation">
            5. App nameに名前を入力して、「create app」ボタンを押す。（プロダクト用のパイプライン作成）
          </div>
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
            1. GitHub Pagesを確認する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd41)" />
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
      「New site from Git」を押す。
       `,
      cmd12: `
      リポジトリを選択
      `,
      cmd13: `
      Owner: チーム名
      Branch to deploy: master
      Build command: nuxt generate
      Publish directory: dist
      Deploy site」ボタンを押す。
      Netlifyのサイトにアクセスして確認する
      `,

      cmd21: `
      $ firebase login:ci
      表示されたデプロイ用のFirebaseトークンをコピーする。
      `,
      cmd22: `
      歯車アイコンをクリック
      `,
      cmd23: `
      「Environment Variables」へ遷移
      `,
      cmd24: `
      デプロイ用のFirebaseトークンを
      Circle CIのEnvironment Variables画面の「Add Variable」ボタンを押しポップアップ画面に入力する。
      nema:  FIREBASE_API_KEY 
      value: xxxaoxnMhPCgF8SoK2ND6HDdh4G0-bKm-xxxxxxxxxxxx
      `,
      cmd25: `
      name:  FIREBASE_PROJECT_ID
      value: nuxt-app-xxxxxxxx
      `,
      cmd26: `
      name:  FIREBASE_API_KEY
      value: xxxxxxxxx_zE8_oNkN43OS-xhlIIAQv2uOjLTLI 
 
      name:  FIREBASE_AUTH_DOMAIN
      value: nuxt-app-xxxx.firebaseapp.com
 
      name:  FIREBASE_DATABASEURL
      value: https://nuxt-app-xxxx.firebaseio.com
 
      name:  FIREBASE_PROJECTID
      value: nuxt-app-xxxx
 
      name:  FIREBASE_STORAGEBUCKET
      value: nuxt-app-xxxx.appspot.com
      `,
      cmd27: `
      $ npm install --save-dev firebase-tools
      $ npm install --save-dev @nuxtjs/dotenv
      `,
      cmd28: `
      cmd23
      `,
      cmd29: `
      version: 2
      jobs:
        deploy_dev: # ジョブ名
            docker:
              - image: circleci/node:10.15.3 # ジョブ実行環境のDockerイメージを記述
      steps:
      - checkout # ソースコードのチェックアウト
      - run:
        name: Add env # .envを作成セキュリティのためGitHubにはアップしない
        command: |
            echo "FIREBASE_API_KEY=$FIREBASE_API_KEY" > .env
            echo "FIREBASE_AUTH_DOMAIN=$FIREBASE_AUTH_DOMAIN" >> .env
            echo "FIREBASE_DATABASE_URL=$FIREBASE_DATABASE_URL" >> .env
            echo "FIREBASE_PROJECT_ID=$FIREBASE_PROJECT_ID" >> .env
            echo "FIREBASE_STORAGE_BUCKET=$FIREBASE_STORAGE_BUCKET" >> .env
          # echo "FIREBASE_MESSAGING_SENDER_ID=$FIREBASE_MESSAGING_SENDER_ID" >> .env
      - run: # 順に実行したいコマンドとコマンドに名前をつけます
          name: npm install
          command: npm i
      - run:
          name: build
          command: npm run generate
      - run: # プロジェクト上のfirebase-toolsでデプロイします
          name: deploy to Firebase Hosting
          command: ./node_modules/.bin/firebase deploy --project=$FIREBASE_PROJECT_ID --token=$FIREBASE_TOKEN 
      workflows:
        version: 2
            deploy_dev: # ワークフローの名前
                jobs:
                    - deploy_dev: # 上で定義したジョブを指定します
                        filters:
                            branches:
                                # developブランチのみを実行対象とします。今回はdevブランチ
                                only: dev 
      `,
      cmd210: `
      cmd23
      `,
      cmd211: `
      cmd23
      `,
      cmd212: `
      cmd23
      `,
      cmd41: `
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
.deploy{
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
