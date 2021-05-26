<template>
  <v-row justify="center" align="center" class="my-5 px-10">
    <v-container class="text-center">
      <v-col cols="12">
        <h1 class="display-1 font-weight"><router-link to="/skills">Skills</router-link></h1>
      </v-col>
    </v-container>

    <v-col
      v-for="(item, i) in items"
      :key="i"
      cols="12" sm="12" md="4" lg="4" xl="4"
    >
      <v-card
        class="mx-auto"
        height="425"
      >
        <template slot="progress">
          <v-progress-linear
            color="deep-purple"
            height="10"
            indeterminate
          ></v-progress-linear>
        </template>

        <v-img
          :aspect-ratio="361/267"
          height="250"
          :src="item.image"
        >
          <template v-slot:placeholder>
            <v-row
              class="fill-height ma-0"
              align="center"
              justify="center"
            >
              <v-progress-circular
                indeterminate
                color="grey lighten-5"
              ></v-progress-circular>
            </v-row>
          </template>
        </v-img>

        <v-card-title class="my-２">{{item.title}}</v-card-title>
        <v-card-text>
          <p>{{item.text}}</p>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          image: require("@/assets/img/front-end.jpg"),
          title: "フロントエンド",
          text: "HTML、CSSをはじめ、VueやReactなどのフロントエンドフレームワークを扱うこともできます。"
        },
        {
          image: require("@/assets/img/back-end.jpg"),
          title: "バックエンド",
          text: "主にNode.jsを使用して開発しています。最近はGo言語の勉強もしており、Go言語を使ったプロジェクトに携わることが直近の目標です。",
        },
        {
          image: require("@/assets/img/cloud.jpg"),
          title: "クラウドサービス",
          text: "AWSの基本サービス（EC2やVPC、ECR、ECS等）の基礎知識を有しています。このポートフォリオサイトはAWS Fargateを使用してホストされています。",
        },
      ]
    }
  }
}
</script>
