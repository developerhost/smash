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

        <v-col cols="12">
          <!-- 変数valueにキャラ名(マリオ)が入る -->
          <v-autocomplete
            v-model="value"
            :items="items"
            dense
            filled
            label="Filled"
          ></v-autocomplete>
        </v-col>
      </v-col>

      <v-col class="mb-5" cols="12">
        <!-- メソッドで％のfunction作るifマリオ→50% -->
        <p v-if="value !== null">
          <!-- {{マリオ}}の場合、ジャンプ投げ空上は{{~65%}}、２段ジャンプ空上は{{~76%}}で確定します -->
          {{ value }}の場合、ジャンプ投げ空上は{{ jump() }}、２段ジャンプ空上は{{ jump2() }}で確定します
        </p>
        <p v-else>
          キャラを選択してください
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
    value: null,
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
      "ソニック",
      "デデデ",
      "ピクミン＆オリマー",
      "ルカリオ",
      "ロボット",
      "トゥーンリンク",
      "ウルフ",
      "むらびと",
      "ロックマン",
      "Wii Fit トレーナー",
      "Wii Fir トレーナー　腹式呼吸",
      "ロゼッタ＆チコ",
      "リトル・マック",
      "ゲッコウガ",
      "パルテナ",
      "パックマン",
      "ルフレ",
      "シュルク通常/疾",
      "シュルク翔/斬",
      "シュルク盾",
      "シュルク撃",
      "クッパ Jr.",
      "ダックハント",
      "リュウ/ケン",
      "クラウド",
      "カムイ",
      "ベヨネッタ",
      "インクリング",
      "リドリー",
      "シモン/リヒター",
      "キングクルール",
      "しずえ",
      "ガオガエン",
      "パックンフラワー",
      "ジョーカー",
      "勇者",
      "勇者バイキルト",
      "勇者ピオリム",
      "バンジョー＆カズーイ",
      "テリー",
      "べレト/ベレス",
      "ミェンミェン",
      "スティーブ",
      "セフィロス",
      "格闘Mii",
      "剣術Mii",
      "射撃Mii",
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
  methods: {
    jump:function(){
      console.log(this.value);
      if(this.value == "マリオ"){
        return "~65%"
      }
    },
    jump2:function(){
        if(this.value == "マリオ"){
        return "~76%"
      }
    }
  }
};
</script>

<style scoped>
.word {
  margin: 10px 10px 10px 10px;
    border: 3px double #ddd;
    padding: 2px;
}
</style>
