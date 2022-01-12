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
            label="相手キャラを入力してください"
          ></v-autocomplete>
        </v-col>
      </v-col>

      <v-col class="mb-5" cols="12">
        <!-- メソッドで％のfunction作るifマリオ→50% -->
        <p v-if="value !== null">
          <!-- {{マリオ}}の場合、ジャンプ投げ空上は{{~65%}}、２段ジャンプ空上は{{~76%}}で確定します -->
          {{ value }}の場合、ジャンプ投げ空上は{{ jump() }}、２段ジャンプ空上は{{ jump2() }}で確定します
          <br>
          ポケスタ２台上の場合、ジャンプ投げ空上は{{ poke() }}、２段ジャンプ空上は{{ poke2() }}で確定します。
          <br>
          ポケスタ２台下/終点の場合、ジャンプ投げ空上は{{ end() }}、２段ジャンプ空上は{{ end() }}で確定します。
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
      "キャプテン・ファルコン",
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
      "Wii Fir トレーナー腹式呼吸",
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
      } else if(this.value == "ドンキーコング"){
        return "~84%"
      } else if(this.value == "リンク"){
        return "~72%"
      } else if(this.value == "サムス/ダークサムス"){
        return "~77%"
      } else if(this.value == "ヨッシー"){
        return "~64%"
      } else if(this.value == "カービィ"){
        return "~60%"
      } else if(this.value == "フォックス"){
        return "~54%"
      } else if(this.value == "ピカチュウ"){
        return "~53%"
      } else if(this.value == "ルイージ"){
        return "~65%"
      } else if(this.value == "ネス"){
        return "~64%"
      } else if(this.value == "キャプテン・ファルコン"){
        return "~78%"
      } else if(this.value == "プリン"){
        return "~58%"
      } else if(this.value == "ピーチ/デイジー"){
        return "~61%"
      } else if(this.value == "クッパ"){
        return "~90%"
      } else if(this.value == "アイスクライマー"){
        return "~60%"
      } else if(this.value == "シーク"){
        return "~60%"
      } else if(this.value == "ゼルダ"){
        return "~60%"
      } else if(this.value == "ドクターマリオ"){
        return "~65%"
      } else if(this.value == "ピチュー"){
        return "~53%"
      } else if(this.value == "ファルコ"){
        return "~55%"
      } else if(this.value == "マルス/ルキナ"){
        return "~66%"
      } else if(this.value == "こどもリンク"){
        return "~63%"
      } else if(this.value == "ガノンドロフ"){
        return "~84%"
      } else if(this.value == "ミュウツー"){
        return "~63%"
      } else if(this.value == "ロイ/クロム"){
        return "~68%"
      } else if(this.value == "Mr.ゲーム＆ウォッチ"){
        return "~53%"
      } else if(this.value == "メタナイト"){
        return "~57%"
      } else if(this.value == "ピット/ブラックピット"){
        return "~64%"
      } else if(this.value == "ゼロスーツサムス"){
        return "~65%"
      } else if(this.value == "ワリオ"){
        return "~69%"
      } else if(this.value == "スネーク"){
        return "~81%"
      } else if(this.value == "アイク"){
        return "~78%"
      } else if(this.value == "ゼニガメ"){
        return "~54%"
      } else if(this.value == "フシギソウ"){
        return "~63%"
      } else if(this.value == "リザードン"){
        return "~79%"
      } else if(this.value == "ディディーコング"){
        return "~61%"
      } else if(this.value == "リュカ"){
        return "~65%"
      } else if(this.value == "ソニック"){
        return "~61%"
      } else if(this.value == "デデデ"){
        return "~87%"
      } else if(this.value == "ピクミン＆オリマー"){
        return "~54%"
      } else if(this.value == "ルカリオ"){
        return "~71%"
      } else if(this.value == "ロボット"){
        return "~82%"
      } else if(this.value == "トゥーンリンク"){
        return "~59%"
      } else if(this.value == "ウルフ"){
        return "~66%"
      } else if(this.value == "むらびと"){
        return "~60%"
      } else if(this.value == "ロックマン"){
        return "~71%"
      } else if(this.value == "Wii Fit トレーナー"){
        return "~68%"
      } else if(this.value == "Wii Fit トレーナー腹式呼吸"){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      } else if(this.value == ""){
        return "~%"
      }
    },
    jump2:function(){
        if(this.value == "マリオ"){
        return "~76%"
      }else if(this.value == "ドンキーコング"){
        return "~97%"
      }
    },
    poke:function(){

    },
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
