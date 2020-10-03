<template>
  <v-footer app absolute padless color="black">
    <v-container class="my-5 grey--text text--lighten-5">
      <v-row>
        <p class="mt-3 mb-1 mx-auto">
          Copyright&nbsp;&copy;&nbsp;
          <span id="year-info" />
          <a
            href="https://github.com/sunxiaolong321"
            target="_blank"
            title="博客作者的Github"
            >logoo</a
          >.&nbsp;Powered&nbsp;by&nbsp;Django.
        </p>
      </v-row>
      <v-row>
        <p class="mb-5 mx-auto">
          <a href="#" target="_blank">benian</a>&nbsp;|
          <a href="#" target="_blank">Sitemap</a>
          网站地图
          <span id="web-day">| {{ getNewYear() }}</span>
        </p>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  methods: {
    getNewYear() {
      const d = new Date()
      const old = new Date('2020/10/02')
      const dd = Math.floor((d.getTime() - old.getTime()) / (24 * 3600 * 1000))
      const dstr = '网站已续航 ' + dd + ' 天'
      return dstr
    },
  },
}
</script>

<style scoped>
a {
  color: white;
}
a:hover {
  color: #81D4FA;
}
</style>
