<template>
  <v-card outlined hover>
    <v-card-title class="justify-center">文章标签</v-card-title>
    <v-divider class="mx-2 my-1" />
    <v-card-text>
      <v-btn
        v-for="(tag, i) in tags"
        :key="i"
        outlined
        small
        class="body-2 text-center mr-2 mb-2"
        >{{ tag }}</v-btn
      >
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    tags: ['Python', 'VUE', 'JS', 'CSS'],
  }),
}
</script>
