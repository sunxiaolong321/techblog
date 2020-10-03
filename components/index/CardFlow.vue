<template>
  <v-card outlined hover nuxt to="post/1">
    <v-responsive :aspect-ratio="16 / 4">
      <v-card-title class="justify-center">{{ title }}</v-card-title>
      <v-card-subtitle class="text-center font-weight-thin"
        ><span class="mr-3">{{ author }}</span
        ><span>{{ post_time }}</span></v-card-subtitle
      >
      <v-card-text class="body-1 font-weight-light mx-1">{{
        summary
      }}</v-card-text>
      <v-divider class="mx-5 my-1" />
      <v-row align="center" class="mx-3">
        <v-col class="text-left text-caption font-weight-light">
          <v-chip v-for="(tag, i) in tags" :key="i" outlined class="mr-2">
            {{ tag }}
          </v-chip>
        </v-col>
        <v-col class="text-right text-caption font-weight-light">{{
          modified_time
        }}</v-col>
      </v-row>
    </v-responsive>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    title: '测试代码',
    summary: '测试简介',
    author: '我',
    post_time: '今天',
    tags: ['Python', 'rss'],
    modified_time: '2020年10月02日',
  }),
}
</script>
