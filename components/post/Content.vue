<template>
  <v-card outlined>
    <div class="mx-6 pt-4 pb-2 font-weight-light text-subtitle-2">
      <span>发布时间：{{ published_time }}</span>
      <span>分类：{{ category }}</span>
      <span>{{ read_count }}阅读</span>
    </div>
    <v-divider class="mx-2 my-1" />
    <nuxt-content :document="$props.content" class="mx-6 my-6 pb-5" />
  </v-card>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      required: true,
    },
  },
  data: () => ({
    published_time: '2020年9月10日',
    category: 'JavaScript',
    read_count: 61,
  }),
}
</script>

<style scoped>
span {
  margin-right: 1rem;
}
</style>
