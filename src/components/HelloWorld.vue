<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-1 font-weight-bold mb-3">リフコン％表示ツール</h1>

        <v-text-field
          label="相手キャラを入力"
          placeholder="マリオ"
        ></v-text-field>

        <v-select :items="items" label="相手キャラを選択">{{ select.character }}</v-select>

        <!-- 入力部分 -->
        相手キャラ→<input class="word" type="text" list="item" placeholder="相手キャラを入力"/>

        <!-- リスト部分 -->
        <datalist id="item">
          <option value="マリオ"></option>
          <option value="ドンキーコング"></option>
          <option value="リンク"></option>
        </datalist>
      </v-col>

      <v-col class="mb-5" cols="12">
        <p>
          <!-- {{マリオ}}の場合、ジャンプ投げ空上は{{~65%}}、２段ジャンプ空上は{{~76%}}で確定します -->
          {{ select.character }}の場合、ジャンプ投げ空上は{{ select.J }}、２段ジャンプ空上は{{ select.JJ }}で確定します
        </p>
      </v-col>

      <v-col class="mb-5" cols="12">

      </v-col>

      <v-col class="mb-5" cols="12">
        
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({

    select: [
      {"character": "マリオ",
        "J": "~65%",
        "JJ": "~76%"
      },

    ],

    items: [
      "マリオ",
      "ドンキーコング",
      "サムス/ダークサムス",
      "ダークサムス",
      "ヨッシー",
      "カービィ",
      "フォックス",
      "ピカチュウ",
      "ルイージ",
      "ネス",
      "キャプテンファルコン",
      "プリン",
      "ピーチ/デイジー",
      "クッパ",
      "アイスクライマー",
      "シーク",
      "ゼルダ",
      "ドクターマリオ",
      "ピチュー",
      "ファルコ",
      "マルス/ルキナ",
      "こどもリンク",
      "ガノンドロフ",
      "ミュウツー",
      "ロイ/クロム",
      "Mr.ゲーム＆ウォッチ",
      "メタナイト",
      "ピット/ブラックピット",
      "ゼロスーツサムス",
      "ワリオ",
      "スネーク",
      "アイク",
      "ゼニガメ",
      "フシギソウ",
      "リザードン",
      "ディディーコング",
      "リュカ",
      "",
      "",
      "",
      "",
      "",
      "",
      "",
    ],

    ecosystem: [
      {
        text: "vuetify-loader",
        href: "https://github.com/vuetifyjs/vuetify-loader",
      },
      {
        text: "github",
        href: "https://github.com/vuetifyjs/vuetify",
      },
      {
        text: "awesome-vuetify",
        href: "https://github.com/vuetifyjs/awesome-vuetify",
      },
    ],
    importantLinks: [
      {
        text: "Documentation",
        href: "https://vuetifyjs.com",
      },
      {
        text: "Chat",
        href: "https://community.vuetifyjs.com",
      },
      {
        text: "Made with Vuetify",
        href: "https://madewithvuejs.com/vuetify",
      },
      {
        text: "Twitter",
        href: "https://twitter.com/vuetifyjs",
      },
      {
        text: "Articles",
        href: "https://medium.com/vuetify",
      },
    ],
    whatsNext: [
      {
        text: "Explore components",
        href: "https://vuetifyjs.com/components/api-explorer",
      },
      {
        text: "Select a layout",
        href: "https://vuetifyjs.com/getting-started/pre-made-layouts",
      },
      {
        text: "Frequently Asked Questions",
        href: "https://vuetifyjs.com/getting-started/frequently-asked-questions",
      },
    ],
  }),
};
</script>

<style scoped>
.word {
  margin: 10px 10px 10px 10px;
    border: 3px double #ddd;
    padding: 2px;
}
</style>
