<template>
    <v-img :src="require('@/assets/img/top.png')" max-height="600" dark>
      <v-row
        align="center"
        justify="center"
      >
        <v-col
          class="text-center"
          cols="12"
        >
          <h1 class="display-2 font-weight-light mb-4">
            Keisuke's Portfolio
          </h1>
          <h4>
            IT技術で社会に貢献する
          </h4>
        </v-col>
      </v-row>
    </v-img>
</template>

<style>
.v-main__wrap > .container {
  max-width: 100%;
}
#app > div > main > div > div > div > div.v-image.v-responsive.theme--dark > div.v-responsive__content {
  display: flex;
}
</style>
