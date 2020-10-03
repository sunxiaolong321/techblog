<template>
  <v-card outlined>
    <div class="text-h4 pl-6 pt-6">
      {{ title }}
    </div>
    <v-breadcrumbs
      :items="breadcrumbs"
      divider="》"
      class="pt-3 pb-6"
    ></v-breadcrumbs>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    title: '测试标题',
    breadcrumbs: [
      {
        text: 'Dashboard',
        disabled: false,
        href: 'breadcrumbs_dashboard',
      },
      {
        text: 'Link 1',
        disabled: false,
        href: 'breadcrumbs_link_1',
      },
      {
        text: 'Link 2',
        disabled: true,
        href: 'breadcrumbs_link_2',
      },
    ],
  }),
}
</script>
