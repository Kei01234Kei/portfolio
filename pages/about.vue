<template>
  <v-container>
    <v-row justify="center" align="center" class="my-5 mx-3">
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h1 class="display-1 font-weight">About</h1>
      </v-col>
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <p>岐阜大学にて情報工学を専攻しています。得意分野はweb系です。ReactやVueなどのフロントエンドフレームワークやNuxtなどのwebアプリケーションフレームワーク、AWSなどのクラウド技術等、さまざまな経験を有しています。</p>
      </v-col>
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h4>名前: 石上 敬祐</h4>
        <h4>所在地: 岐阜県</h4>
        <h4>お問い合わせ: <a href="mailto:keisuke.130@icloud.com">keisuke.130@icloud.com</a></h4>
      </v-col>
    </v-row>
    <v-row justify="center" align="center" class="my-5 mx-3">
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h1 class="display-1 font-weight">Education</h1>
      </v-col>
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h2>東京農業大学第二高等学校 普通科</h2>
        <p>2017年4月〜2020年3月</p>
      </v-col>
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h2>岐阜大学 工学部電気電子・情報工学科情報コース</h2>
        <p>2020年4月〜現在</p>
      </v-col>
    </v-row>
    
    <v-row justify="center" align="center" class="my-5 mx-3">
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h1 class="display-1 font-weight">Skills</h1>
        <v-row justify="center" class="my-2">
          <v-col
            v-for="(item, i) in items"
            :key="i"
            cols="12" sm="12" md="4" lg="4" xl="4"
          >
            <v-card
              class="mx-auto"
              max-width="344"
            >
              <v-img
                :src="item.image"
                height="200px"
              ></v-img>
              <v-card-actions>
                <v-card-title>
                  {{item.title}}
                </v-card-title>
                <v-spacer></v-spacer>
                <v-btn
                  icon
                  @click="item.show = !item.show"
                >
                  <v-icon>{{ item.show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn>
              </v-card-actions>
              <v-expand-transition>
                <div v-show="item.show">
                  <v-divider></v-divider>
                  <v-card-text>
                    {{item.text}}
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row justify="center" align="center" class="my-5 mx-3">
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h1 class="display-1 font-weight">Activity</h1>
      </v-col>
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <p>ICPC2020国内予選</p>
        <p>Open Hack U 2020 Online Vol.4</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          image: require("@/assets/img/front-end.jpg"),
          title: "フロントエンド",
          text: "webページ作成の際には主にNuxt.jsを使用しています。まだ業務経験は少ないですが、Reactを扱うこともできます。",
          show: false,
        },
        {
          image: require("@/assets/img/back-end.jpg"),
          title: "バックエンド",
          text: "主にNode.jsを使用して開発しています。また、Fireaseを使って大学の講義レビューサイトを作った経験もあります。この講義レビューサイト開発を通じて、ユーザ認証やデータベースの扱い方など、webアプリ開発のための基礎的な技術を学びました。",
          show: false,
        },
        {
          image: require("@/assets/img/cloud.jpg"),
          title: "クラウドサービス",
          text: "AWSの基本サービス（EC2やVPC、ECR、ECS等）の基礎知識を有しています。このポートフォリオサイトはAWS Fargateを使用してホストしています。このポートフォリオ作成過程で、ロードバランサーやオートスケーリングに関する知見も得ることができました。",
          show: false,
        },
      ]
    }
  }
}
</script>
