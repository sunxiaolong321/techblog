<template>
  <v-container>
    <v-row justify="center">
      <v-col lg="10" md="12" sm="12">
        <post-title />
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col lg="10" md="12" sm="12">
        <post-content :content="page" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  components: {
    postTitle: () => import('@/components/post/Title'),
    postContent: () => import('@/components/post/Content'),
  },
  async asyncData({ $content }) {
    const page = await $content('articles', 'hello').fetch()
    return {
      page,
    }
  },
  validate({ params }) {
    return /^\d+$/.test(params.id)
  },
}
</script>
