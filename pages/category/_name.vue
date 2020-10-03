<template>
  <section>
    <v-card
      class="mx-auto"
      max-width="344" v-for="(article,key) in articles" :key="key"
    >
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
      ></v-img>

      <v-card-title>
        {{ article.title }}
      </v-card-title>

      <v-card-subtitle>
        {{ article.summary }}
      </v-card-subtitle>

      <v-card-actions>
        <v-btn text>{{ article.viewCounts }}</v-btn>
      </v-card-actions>
    </v-card>
  </section>
</template>
<script>
import axios from 'axios'

export default {
  validate({params}) {
    console.log(params);
    if (!params.name) {
      return false;
    }
    return /^\w+$/.test(params.name);
  },
  async asyncData({params}) {
    const {data} = await axios.get(
      `http://localhost:8080/api/articles/category/${params["name"]}`
    );
    return {articles: data.data};
  },
};
</script>
