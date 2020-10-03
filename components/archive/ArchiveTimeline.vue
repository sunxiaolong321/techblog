<template>
  <v-timeline clipped>
    <v-timeline-item
      v-for="(item, key) in timeline"
      :key="key"
      color="orange"
      class="mb-12"
    >
      <template v-slot:opposite>
        <span>{{ item.time }}</span>
      </template>
      <v-card class="elevation-2">
        <v-card-title class="headline">{{ item.title }}</v-card-title>
        <v-card-text>{{ item.summary }}</v-card-text>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
export default {
  data: () => ({
    form_data: {
      time: '2000年1月1日',
      title: '',
      summary: '',
    },
    timeline: [],
  }),
}
</script>
