<template>
  <v-app>
    <Bar />
    <v-main>
      <nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  components: {
    Bar: () => import('@/components/global/Bar'),
    Footer: () => import('@/components/global/Footer'),
  },
}
</script>
