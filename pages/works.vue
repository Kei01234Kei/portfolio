<template>
  <v-container>
    <v-row justify="center" align="center" class="my-5 mx-3">
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <h1 class="display-1 font-weight">Works</h1>
      </v-col>
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <p>web系のアプリ、サービスをメインに作っています。これらの作品の中にはチームで開発したものも含まれています。</p>
      </v-col>
    </v-row>

    <v-row justify="center" align="center" class="mx-3">
      <v-col cols="12" sm="12" md="10" lg="10" xl="8">
        <v-row justify="center" class="my-2">
          <v-col
            v-for="(item, i) in items"
            :key="i"
            cols="12" sm="12" md="6" lg="6" xl="6"
          >
            <a v-bind:href="item.url">
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
                  class="blue-grey--text text--lighten-5 align-end"
                  height="300"
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
                  <v-card-title class="font-weight-bold">{{item.title}}</v-card-title>
                </v-img>
              </v-card>
            </a>
          </v-col>
        </v-row>
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
          url: "https://fulltan-navi.com/",
          image: require("@/assets/img/fulltan-navi.png"),
          title: "フル単ナビ",
        },
        {
            url: "https://portfolio.keisuke.app",
            image: require("@/static/ogpImage.png"),
            title: "Keisuke's Portfolio",

        },
      ]
    }
  }
}
</script>
