<template>
  <nav-card />
</template>

<script>
export default {
  components: {
    navCard: () => import('@/components/navigation/NavCard'),
  },
}
</script>
