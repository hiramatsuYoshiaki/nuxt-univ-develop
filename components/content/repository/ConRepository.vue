<template>
  <div class="repository">
    <div class="flex-container">
      <div class="side-col">
        <a href="#a1">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 1}" @click="menuActive(1)">
            1. リモートリポジトリをcloneする。
          </p>
        </a>
        <a href="#a2">
          <p class="topMenu topMenu1" :class="{ activeTopMenu : selectMenu === 2}" @click="menuActive(2)">
            2. 新規リポジトリを作成する。
          </p>
        </a>
      </div>

      <div class="main-col">
        <div id="a1" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            1. リモートリポジトリをcloneする。
          </div>
          <!-- <div class="mainTitle">
            <div class="h3-res">
              GitHubリポジトリをcloneしてローカルプロジェクトを作る
            </div>
          </div> -->
          <div class="mainDescription">
            <p>プロジェクトホルダーを作成し、GitHubリポジトリをcloneしてローカルプロジェクトを作る</p>
          </div>
          <div class="mainOperation">
            1. リモートリポジトリをcloneする。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd11)" />
            </div>
          </div>
          <div class="mainOperation">
            2. インストールする
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd12)" />
            </div>
          </div>
          <div class="mainOperation">
            3. サーバーを立ち上げて確認
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd13)" />
            </div>
          </div>
          <div class="mainOperation">
            4. ローカルサーバーへアクセス
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd14)" />
            </div>
          </div>
        </div>

        <div id="a2" />
        <div class="main-wrap">
          <div class="topMain h1-res">
            2. 新規リポジトリを作成する。
          </div>
          <!-- <div class="mainTitle">
            <div class="h3-res">
              新規プロジェクト用のリポジトリを作り、チーム開発のバージョン管理を行います。
            </div>
          </div> -->
          <div class="mainDescription">
            <p>GitHubリポジトリにプロジェクトを作り、プッシュします。</p>
          </div>
          <div class="mainOperation">
            1. GitHub ログイン後のトップページから、Repositories の New ボタンをクリックします。
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd21)" />
            </div>
          </div>

          <div class="mainOperation">
            2. Create a new repository の画面に遷移するので、リポジトリ名、ライセンス等を入力する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd22)" />
            </div>
          </div>
          <div class="mainOperation">
            3. プロジェクトを GitHub に Push する
          </div>
          <div class="mainComandWrap">
            <div class="mainComand">
              <div v-html="$md.render(cmd23)" />
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
.repository{
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
