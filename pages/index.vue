<template>
  <v-row justify="center" align="center">
    <topImage />
    <about />
    <skills />
    <works />
  </v-row>
</template>

<script>
import topImage from '@/components/topImage.vue'
import about from '@/components/about.vue'
import skills from '@/components/skills.vue'
import works from '@/components/works.vue'

export default {
  components: {
    topImage,
    about,
    skills,
    works,
  }
}
</script>
