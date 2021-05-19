<template>
    <v-row justify="center" align="center" class="my-5 mx-3">
        <v-container class="text-center">
            <v-col cols="12">
        <h1 class="display-1 font-weight"><router-link to="/about">About</router-link></h1>
      </v-col>
            <v-col>
                <p>
                    岐阜大学工学部電気電子・情報工学科情報コース2年の石上敬祐です。<br>
                    国際大学対抗プログラミングコンテストやYahoo! JAPAN主催のハッカソンなど、さまざまなイベントに参加してプログラミング技術を磨いています。<br>
                </p>
            </v-col>
            <v-avatar size="150">
                <v-img :src="require('@/assets/img/avatar.JPG')"></v-img>
            </v-avatar>
        </v-container>
    </v-row>
</template>
