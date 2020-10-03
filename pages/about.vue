<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" lg="7" md="7" sm="12" class="ma-1">
        <v-card outlined hover class="py-6 font-weight-light"
          ><nuxt-content :document="aboutme" /></v-card
      ></v-col>
      <v-col cols="12" lg="3" md="3" sm="12" class="ma-1">
        <card-search class="mb-7" />
        <card-tag class="my-7" />
        <card-calendar class="my-7" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  components: {
    cardSearch: () => import('@/components/index/CardSearch'),
    cardTag: () => import('@/components/index/CardTag'),
    cardCalendar: () => import('@/components/index/CardCalendar'),
  },
  async asyncData({ $content }) {
    const aboutme = await $content('aboutme').fetch()
    return {
      aboutme,
    }
  },
}
</script>
