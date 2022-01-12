<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/donkey.png')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      
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
      
      

      <v-col class="mb-2" cols="12">
        <!-- メソッドで％のfunction作るifマリオ→50% -->
        <div class="font-weight-bold text-left" v-if="value !== null">
          <!-- {{マリオ}}の場合、ジャンプ投げ空上は{{~65%}}、２段ジャンプ空上は{{~76%}}で確定します -->
          {{ value }}の場合、
            <p class="my-3">
            ・ジャンプ投げ空上は <span class="text-h4 font-weight-black">{{ jump() }}</span>、
            </p>

            <p>
            ・２段ジャンプ空上は <span class="text-h4 font-weight-black">{{ jump2() }}</span>で確定します
            </p>

            <p>
            ポケスタ台上の場合、
            </p>

            <p>
            ・ジャンプ投げ空上は <span class="text-h4 font-weight-black">{{ poke() }}</span>、
            </p>

            <p>
            ・２段ジャンプ空上は <span class="text-h4 font-weight-black">{{ poke2() }}</span>で確定します。
            </p>
          
        </div>
        <div class="font-weight-medium" v-else>
          キャラを選択してください
        </div>
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
      "クッパJr.",
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
        return "~69%"
      } else if(this.value == "ロゼッタ＆チコ"){
        return "~58%"
      } else if(this.value == "リトル・マック"){
        return "~64%"
      } else if(this.value == "ゲッコウガ"){
        return "~61%"
      } else if(this.value == "パルテナ"){
        return "~65%"
      } else if(this.value == "パックマン"){
        return "~59%"
      } else if(this.value == "ルフレ"){
        return "~71%"
      } else if(this.value == "シュルク通常/疾"){
        return "~73%"
      } else if(this.value == "シュルク翔/斬"){
        return "~69%"
      } else if(this.value == "シュルク盾"){
        return "~223%"
      } else if(this.value == "シュルク撃"){
        return "~33%"
      } else if(this.value == "クッパJr."){
        return "~74%"
      } else if(this.value == "ダックハント"){
        return "~59%"
      } else if(this.value == "リュウ/ケン"){
        return "~79%"
      } else if(this.value == "クラウド"){
        return "~70%"
      } else if(this.value == "カムイ"){
        return "~70%"
      } else if(this.value == "ベヨネッタ"){
        return "~66%"
      } else if(this.value == "インクリング"){
        return "~64%"
      } else if(this.value == "リドリー"){
        return "~86%"
      } else if(this.value == "シモン/リヒター"){
        return "~79%"
      } else if(this.value == "キングクルール"){
        return "~90%"
      } else if(this.value == "しずえ"){
        return "~61%"
      } else if(this.value == "ガオガエン"){
        return "~81%"
      } else if(this.value == "パックンフラワー"){
        return "~71%"
      } else if(this.value == "ジョーカー"){
        return "~67%"
      } else if(this.value == "勇者"){
        return "~70%"
      } else if(this.value == "勇者バイキルト"){
        return "~70%"
      } else if(this.value == "勇者ピオリム"){
        return "~50%"
      } else if(this.value == "バンジョー＆カズーイ"){
        return "~72%"
      } else if(this.value == "テリー"){
        return "~85%"
      } else if(this.value == "べレト/ベレス"){
        return "~64%"
      } else if(this.value == "ミェンミェン"){
        return "~74%"
      } else if(this.value == "スティーブ"){
        return "~64%"
      } else if(this.value == "セフィロス"){
        return "~53%"
      } else if(this.value == "格闘Mii"){
        return "~60%"
      } else if(this.value == "剣術Mii"){
        return "~63%"
      } else if(this.value == "射撃Mii"){
        return "~67%"
      } else {
        return "-"
      }
    },


    jump2:function(){
    if(this.value == "マリオ"){
        return "~76%"
      } else if(this.value == "ドンキーコング"){
        return "~97%"
      } else if(this.value == "リンク"){
        return "~84%"
      } else if(this.value == "サムス/ダークサムス"){
        return "~90%"
      } else if(this.value == "ヨッシー"){
        return "~76%"
      } else if(this.value == "カービィ"){
        return "~70%"
      } else if(this.value == "フォックス"){
        return "~67%"
      } else if(this.value == "ピカチュウ"){
        return "~65%"
      } else if(this.value == "ルイージ"){
        return "~76%"
      } else if(this.value == "ネス"){
        return "~76%"
      } else if(this.value == "キャプテン・ファルコン"){
        return "~89%"
      } else if(this.value == "プリン"){
        return "~69%"
      } else if(this.value == "ピーチ/デイジー"){
        return "~73%"
      } else if(this.value == "クッパ"){
        return "~101%"
      } else if(this.value == "アイスクライマー"){
        return "~71%"
      } else if(this.value == "シーク"){
        return "~71%"
      } else if(this.value == "ゼルダ"){
        return "~70%"
      } else if(this.value == "ドクターマリオ"){
        return "~76%"
      } else if(this.value == "ピチュー"){
        return "~62%"
      } else if(this.value == "ファルコ"){
        return "~64%"
      } else if(this.value == "マルス/ルキナ"){
        return "~75%"
      } else if(this.value == "こどもリンク"){
        return "~74%"
      } else if(this.value == "ガノンドロフ"){
        return "~99%"
      } else if(this.value == "ミュウツー"){
        return "~73%"
      } else if(this.value == "ロイ/クロム"){
        return "~81%"
      } else if(this.value == "Mr.ゲーム＆ウォッチ"){
        return "~67%"
      } else if(this.value == "メタナイト"){
        return "~68%"
      } else if(this.value == "ピット/ブラックピット"){
        return "~77%"
      } else if(this.value == "ゼロスーツサムス"){
        return "~77%"
      } else if(this.value == "ワリオ"){
        return "~80%"
      } else if(this.value == "スネーク"){
        return "~96%"
      } else if(this.value == "アイク"){
        return "~89%"
      } else if(this.value == "ゼニガメ"){
        return "~64%"
      } else if(this.value == "フシギソウ"){
        return "~75%"
      } else if(this.value == "リザードン"){
        return "~92%"
      } else if(this.value == "ディディーコング"){
        return "~72%"
      } else if(this.value == "リュカ"){
        return "~77%"
      } else if(this.value == "ソニック"){
        return "~73%"
      } else if(this.value == "デデデ"){
        return "~99%"
      } else if(this.value == "ピクミン＆オリマー"){
        return "~62%"
      } else if(this.value == "ルカリオ"){
        return "~81%"
      } else if(this.value == "ロボット"){
        return "~94%"
      } else if(this.value == "トゥーンリンク"){
        return "~72%"
      } else if(this.value == "ウルフ"){
        return "~77%"
      } else if(this.value == "むらびと"){
        return "~72%"
      } else if(this.value == "ロックマン"){
        return "~82%"
      } else if(this.value == "Wii Fit トレーナー"){
        return "~79%"
      } else if(this.value == "Wii Fit トレーナー腹式呼吸"){
        return "~81%"
      } else if(this.value == "ロゼッタ＆チコ"){
        return "~69%"
      } else if(this.value == "リトル・マック"){
        return "~74%"
      } else if(this.value == "ゲッコウガ"){
        return "~72%"
      } else if(this.value == "パルテナ"){
        return "~77%"
      } else if(this.value == "パックマン"){
        return "~73%"
      } else if(this.value == "ルフレ"){
        return "~82%"
      } else if(this.value == "シュルク通常/疾"){
        return "~81%"
      } else if(this.value == "シュルク翔/斬"){
        return "~77%"
      } else if(this.value == "シュルク盾"){
        return "~243%"
      } else if(this.value == "シュルク撃"){
        return "~43%"
      } else if(this.value == "クッパJr."){
        return "~84%"
      } else if(this.value == "ダックハント"){
        return "~69%"
      } else if(this.value == "リュウ/ケン"){
        return "~92%"
      } else if(this.value == "クラウド"){
        return "~81%"
      } else if(this.value == "カムイ"){
        return "~82%"
      } else if(this.value == "ベヨネッタ"){
        return "~79%"
      } else if(this.value == "インクリング"){
        return "~78%"
      } else if(this.value == "リドリー"){
        return "~99%"
      } else if(this.value == "シモン/リヒター"){
        return "~93%"
      } else if(this.value == "キングクルール"){
        return "~101%"
      } else if(this.value == "しずえ"){
        return "~72%"
      } else if(this.value == "ガオガエン"){
        return "~98%"
      } else if(this.value == "パックンフラワー"){
        return "~86%"
      } else if(this.value == "ジョーカー"){
        return "~78%"
      } else if(this.value == "勇者"){
        return "~82%"
      } else if(this.value == "勇者バイキルト"){
        return "~80%"
      } else if(this.value == "勇者ピオリム"){
        return "~61%"
      } else if(this.value == "バンジョー＆カズーイ"){
        return "~83%"
      } else if(this.value == "テリー"){
        return "~98%"
      } else if(this.value == "べレト/ベレス"){
        return "~78%"
      } else if(this.value == "ミェンミェン"){
        return "~84%"
      } else if(this.value == "スティーブ"){
        return "~77%"
      } else if(this.value == "セフィロス"){
        return "~66%"
      } else if(this.value == "格闘Mii"){
        return "~69%"
      } else if(this.value == "剣術Mii"){
        return "~76%"
      } else if(this.value == "射撃Mii"){
        return "~80%"
      } else {
        return "-"
      }
    },

    poke:function(){
      if(this.value == "マリオ"){
        return "51%~"
      } else if(this.value == "ドンキーコング"){
        return "65%~"
      } else if(this.value == "リンク"){
        return "55%~"
      } else if(this.value == "サムス/ダークサムス"){
        return "57%~"
      } else if(this.value == "ヨッシー"){
        return "54%~"
      } else if(this.value == "カービィ"){
        return "42%~"
      } else if(this.value == "フォックス"){
        return "42~%"
      } else if(this.value == "ピカチュウ"){
        return "42%~"
      } else if(this.value == "ルイージ"){
        return "51%~"
      } else if(this.value == "ネス"){
        return "50%~"
      } else if(this.value == "キャプテン・ファルコン"){
        return "55%~"
      } else if(this.value == "プリン"){
        return "37%~"
      } else if(this.value == "ピーチ/デイジー"){
        return "48%~"
      } else if(this.value == "クッパ"){
        return "70%~"
      } else if(this.value == "アイスクライマー"){
        return "49%~"
      } else if(this.value == "シーク"){
        return "42%~"
      } else if(this.value == "ゼルダ"){
        return "46%~"
      } else if(this.value == "ドクターマリオ"){
        return "51%~"
      } else if(this.value == "ピチュー"){
        return "35%~"
      } else if(this.value == "ファルコ"){
        return "44%~"
      } else if(this.value == "マルス/ルキナ"){
        return "49%~"
      } else if(this.value == "こどもリンク"){
        return "48%~"
      } else if(this.value == "ガノンドロフ"){
        return "60%~"
      } else if(this.value == "ミュウツー"){
        return "45%~"
      } else if(this.value == "ロイ/クロム"){
        return "51%~"
      } else if(this.value == "Mr.ゲーム＆ウォッチ"){
        return "40%~"
      } else if(this.value == "メタナイト"){
        return "44%~"
      } else if(this.value == "ピット/ブラックピット"){
        return "51%~"
      } else if(this.value == "ゼロスーツサムス"){
        return "45%~"
      } else if(this.value == "ワリオ"){
        return "55%~"
      } else if(this.value == "スネーク"){
        return "56%~"
      } else if(this.value == "アイク"){
        return "56%~"
      } else if(this.value == "ゼニガメ"){
        return "41%~"
      } else if(this.value == "フシギソウ"){
        return "51%~"
      } else if(this.value == "リザードン"){
        return "61%~"
      } else if(this.value == "ディディーコング"){
        return "47%~"
      } else if(this.value == "リュカ"){
        return "50%~"
      } else if(this.value == "ソニック"){
        return "47%~"
      } else if(this.value == "デデデ"){
        return "62%~"
      } else if(this.value == "ピクミン＆オリマー"){
        return "42%~"
      } else if(this.value == "ルカリオ"){
        return "49%~"
      } else if(this.value == "ロボット"){
        return "52%~"
      } else if(this.value == "トゥーンリンク"){
        return "50%~"
      } else if(this.value == "ウルフ"){
        return "50%~"
      } else if(this.value == "むらびと"){
        return "49%~"
      } else if(this.value == "ロックマン"){
        return "55%~"
      } else if(this.value == "Wii Fit トレーナー"){
        return "50%~"
      } else if(this.value == "Wii Fit トレーナー腹式呼吸"){
        return "53%~"
      } else if(this.value == "ロゼッタ＆チコ"){
        return "44%~"
      } else if(this.value == "リトル・マック"){
        return "47%~"
      } else if(this.value == "ゲッコウガ"){
        return "49%~"
      } else if(this.value == "パルテナ"){
        return "49%~"
      } else if(this.value == "パックマン"){
        return "49%~"
      } else if(this.value == "ルフレ"){
        return "52%~"
      } else if(this.value == "シュルク通常/疾"){
        return "51%~"
      } else if(this.value == "シュルク翔/斬"){
        return "44%~"
      } else if(this.value == "シュルク盾"){
        return "162%~"
      } else if(this.value == "シュルク撃"){
        return "27%~"
      } else if(this.value == "クッパJr."){
        return "54%~"
      } else if(this.value == "ダックハント"){
        return "47%~"
      } else if(this.value == "リュウ/ケン"){
        return "51%~"
      } else if(this.value == "クラウド"){
        return "54%~"
      } else if(this.value == "カムイ"){
        return "53%~"
      } else if(this.value == "ベヨネッタ"){
        return "45%~"
      } else if(this.value == "インクリング"){
        return "50%~"
      } else if(this.value == "リドリー"){
        return "56%~"
      } else if(this.value == "シモン/リヒター"){
        return "56%~"
      } else if(this.value == "キングクルール"){
        return "67%~"
      } else if(this.value == "しずえ"){
        return "47%~"
      } else if(this.value == "ガオガエン"){
        return "61%~"
      } else if(this.value == "パックンフラワー"){
        return "55%~"
      } else if(this.value == "ジョーカー"){
        return "49%~"
      } else if(this.value == "勇者"){
        return "53%~"
      } else if(this.value == "勇者バイキルト"){
        return "49%~"
      } else if(this.value == "勇者ピオリム"){
        return "35%~"
      } else if(this.value == "バンジョー＆カズーイ"){
        return "56%~"
      } else if(this.value == "テリー"){
        return "54%~"
      } else if(this.value == "べレト/ベレス"){
        return "52%~"
      } else if(this.value == "ミェンミェン"){
        return "56%~"
      } else if(this.value == "スティーブ"){
        return "50%~"
      } else if(this.value == "セフィロス"){
        return "41%~"
      } else if(this.value == "格闘Mii"){
        return "51%~"
      } else if(this.value == "剣術Mii"){
        return "54%~"
      } else if(this.value == "射撃Mii"){
        return "55%~"
      } else {
        return "-"
      }
    },

    poke2: function() {
      if(this.value == "マリオ"){
        return "67%~"
      } else if(this.value == "ドンキーコング"){
        return "83%~"
      } else if(this.value == "リンク"){
        return "71%~"
      } else if(this.value == "サムス/ダークサムス"){
        return "73%~"
      } else if(this.value == "ヨッシー"){
        return "70%~"
      } else if(this.value == "カービィ"){
        return "57%~"
      } else if(this.value == "フォックス"){
        return "57%~"
      } else if(this.value == "ピカチュウ"){
        return "56%~"
      } else if(this.value == "ルイージ"){
        return "67%~"
      } else if(this.value == "ネス"){
        return "65%~"
      } else if(this.value == "キャプテン・ファルコン"){
        return "71%~"
      } else if(this.value == "プリン"){
        return "51%~"
      } else if(this.value == "ピーチ/デイジー"){
        return "63%~"
      } else if(this.value == "クッパ"){
        return "88%~"
      } else if(this.value == "アイスクライマー"){
        return "64%~"
      } else if(this.value == "シーク"){
        return "58%~"
      } else if(this.value == "ゼルダ"){
        return "61%~"
      } else if(this.value == "ドクターマリオ"){
        return "67%~"
      } else if(this.value == "ピチュー"){
        return "47%~"
      } else if(this.value == "ファルコ"){
        return "58%~"
      } else if(this.value == "マルス/ルキナ"){
        return "63%~"
      } else if(this.value == "こどもリンク"){
        return "62%~"
      } else if(this.value == "ガノンドロフ"){
        return "77%~"
      } else if(this.value == "ミュウツー"){
        return "58%~"
      } else if(this.value == "ロイ/クロム"){
        return "66%~"
      } else if(this.value == "Mr.ゲーム＆ウォッチ"){
        return "54%~"
      } else if(this.value == "メタナイト"){
        return "58%~"
      } else if(this.value == "ピット/ブラックピット"){
        return "66%~"
      } else if(this.value == "ゼロスーツサムス"){
        return "59%~"
      } else if(this.value == "ワリオ"){
        return "70%~"
      } else if(this.value == "スネーク"){
        return "71%~"
      } else if(this.value == "アイク"){
        return "72%~"
      } else if(this.value == "ゼニガメ"){
        return "55%~"
      } else if(this.value == "フシギソウ"){
        return "66%~"
      } else if(this.value == "リザードン"){
        return "77%~"
      } else if(this.value == "ディディーコング"){
        return "62%~"
      } else if(this.value == "リュカ"){
        return "65%~"
      } else if(this.value == "ソニック"){
        return "61%~"
      } else if(this.value == "デデデ"){
        return "80%~"
      } else if(this.value == "ピクミン＆オリマー"){
        return "55%~"
      } else if(this.value == "ルカリオ"){
        return "63%~"
      } else if(this.value == "ロボット"){
        return "71%~"
      } else if(this.value == "トゥーンリンク"){
        return "64%~"
      } else if(this.value == "ウルフ"){
        return "64%~"
      } else if(this.value == "むらびと"){
        return "64%~"
      } else if(this.value == "ロックマン"){
        return "70%~"
      } else if(this.value == "Wii Fit トレーナー"){
        return "66%~"
      } else if(this.value == "Wii Fit トレーナー腹式呼吸"){
        return "69%~"
      } else if(this.value == "ロゼッタ＆チコ"){
        return "58%~"
      } else if(this.value == "リトル・マック"){
        return "62%~"
      } else if(this.value == "ゲッコウガ"){
        return "63%~"
      } else if(this.value == "パルテナ"){
        return "64%~"
      } else if(this.value == "パックマン"){
        return "64%~"
      } else if(this.value == "ルフレ"){
        return "66%~"
      } else if(this.value == "シュルク通常/疾"){
        return "67%~"
      } else if(this.value == "シュルク翔/斬"){
        return "60%~"
      } else if(this.value == "シュルク盾"){
        return "188%~"
      } else if(this.value == "シュルク撃"){
        return "40%~"
      } else if(this.value == "クッパJr."){
        return "70%~"
      } else if(this.value == "ダックハント"){
        return "61%~"
      } else if(this.value == "リュウ/ケン"){
        return "69%~"
      } else if(this.value == "クラウド"){
        return "69%~"
      } else if(this.value == "カムイ"){
        return "68%~"
      } else if(this.value == "ベヨネッタ"){
        return "59%~"
      } else if(this.value == "インクリング"){
        return "65%~"
      } else if(this.value == "リドリー"){
        return "72%~"
      } else if(this.value == "シモン/リヒター"){
        return "73%~"
      } else if(this.value == "キングクルール"){
        return "83%~"
      } else if(this.value == "しずえ"){
        return "62%~"
      } else if(this.value == "ガオガエン"){
        return "78%~"
      } else if(this.value == "パックンフラワー"){
        return "73%~"
      } else if(this.value == "ジョーカー"){
        return "64%~"
      } else if(this.value == "勇者"){
        return "69%~"
      } else if(this.value == "勇者バイキルト"){
        return "65%~"
      } else if(this.value == "勇者ピオリム"){
        return "54%~"
      } else if(this.value == "バンジョー＆カズーイ"){
        return "72%~"
      } else if(this.value == "テリー"){
        return "72%~"
      } else if(this.value == "べレト/ベレス"){
        return "67%~"
      } else if(this.value == "ミェンミェン"){
        return "72%~"
      } else if(this.value == "スティーブ"){
        return "64%~"
      } else if(this.value == "セフィロス"){
        return "55%~"
      } else if(this.value == "格闘Mii"){
        return "65%~"
      } else if(this.value == "剣術Mii"){
        return "68%~"
      } else if(this.value == "射撃Mii"){
        return "70%~"
      } else {
        return "-"
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
