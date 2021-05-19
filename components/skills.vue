<template>
  <v-row justify="center" align="center" class="my-5 px-10">
    <v-container class="text-center">
      <v-col cols="12">
        <h1 class="display-1 font-weight"><router-link to="/skills">Skills</router-link></h1>
      </v-col>
    </v-container>
    <v-col cols="12" sm="12" md="4" lg="4" xl="4">
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
          :src="require('@/assets/img/front-end.jpg')"
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

        <v-card-title class="my-２">フロントエンド</v-card-title>
        <v-card-text>
          <p>HTML、CSSをはじめ、VueやReactなどのフロントエンドフレームワークを扱うこともできます。</p>
        </v-card-text>
      </v-card>
    </v-col>

    <v-col v-col cols="12" sm="12" md="4" lg="4" xl="4">
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
          :src="require('@/assets/img/back-end.jpg')"
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

        <v-card-title class="my-２">バックエンド</v-card-title>
        <v-card-text>
          <p>主にNode.jsを使用して開発しています。最近はGo言語の勉強もしており、Go言語を使ったプロジェクトに携わることが直近の目標です。</p>
        </v-card-text>
      </v-card>
    </v-col>

    <v-col v-col cols="12" sm="12" md="4" lg="4" xl="4">
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
          :src="require('@/assets/img/cloud.jpg')"
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

        <v-card-title class="my-２">クラウドサービス</v-card-title>
        <v-card-text>
          <p>AWSの基本サービス（EC2やVPC、ECR、ECS等）の基礎知識を有しています。また、このポートフォリオサイトはAWS ECSを使用して運営されています。</p>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>
