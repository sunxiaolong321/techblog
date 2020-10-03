<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" lg="5" md="8" sm="12">
        <timeline />
      </v-col>
      <!-- <v-col cols="12" lg="3" md="4" sm="12">
      <personalmsg />
      <categorylist />
      <tag-list />
    </v-col> -->
    </v-row>
  </v-container>
</template>

<script>
export default {
  components: {
    timeline: () => import('@/components/archive/ArchiveTimeline'),
  },
}
</script>
