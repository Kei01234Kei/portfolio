<template>
  <v-row justify="center" align="center" class="my-5 px-10">
    <v-container class="text-center">
      <v-col>
        <h1 class="display-1 font-weight"><router-link to="/works">Works</router-link></h1>
      </v-col>
      <v-col>
        <p>私が開発に携わった主要なサービス一覧です。詳細な開発経験については<a href="https://github.com/Kei01234">私のGitHub</a>をご覧ください。</p>
      </v-col>
    </v-container>
    <v-col cols="12" sm="12" md="4" lg="4" xl="4">
      <a href="https://fulltan-navi.com/">
      <v-hover>
          
      </v-hover>
        <v-card
          class="mx-auto"

        >
          <template slot="progress">
            <v-progress-linear
              color="deep-purple"
              height="10"
              indeterminate
            ></v-progress-linear>
          </template>
          <v-img
            class="blue-grey--text text--darken-3 align-end"
            :aspect-ratio="361/267"
            height="300"
            :src="require('@/assets/img/fulltan-navi.png')"
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
            <v-card-title class="font-weight-bold">フル単ナビ</v-card-title>
          </v-img>
        </v-card>
      </a>
    </v-col>
  </v-row>
</template>
