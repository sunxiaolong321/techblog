<template>
  <v-app-bar app outlined flat hide-on-scroll color="white">
    <v-app-bar-nav-icon class="hidden-md-and-up" />
    <v-toolbar-title class="mr-2" name="个人技术博客"
      >个人技术博客</v-toolbar-title
    >
    <v-spacer />
    <v-btn nuxt to="/" class="hidden-sm-and-down" text> &nbsp;首页 </v-btn>
    <v-btn nuxt to="/archive" class="hidden-sm-and-down" text>
      &nbsp;归档
    </v-btn>
    <v-btn nuxt to="/tools" class="hidden-sm-and-down" text> &nbsp;工具 </v-btn>
    <v-btn nuxt to="/navigation" class="hidden-sm-and-down" text>
      &nbsp;导航
    </v-btn>
    <v-btn nuxt to="/about" class="hidden-sm-and-down" text> &nbsp;关于 </v-btn>
  </v-app-bar>
</template>
