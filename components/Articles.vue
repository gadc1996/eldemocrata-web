<template lang="pug">
 .articles 
    .article(v-for="article in articles")
      img.article__image(src="https://via.placeholder.com/300")
      h2.article__title {{ article.title }}
      // .article__content(v-html="article.content")
</template>

<script>
export default {
  name: 'Articles',
  data: () => ({
    articles: {}
  }),
  mounted() {
     this.loadArticles()
  },
  methods: {
    async loadArticles() {
      const response = await this.$axios.$get('articles')
      this.articles = response.data
    }
  }
}
</script>

<style lang="scss">
$articles-per-row: 3;

.articles {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-gap: 15px;
}

.article {
  grid-column: span ($articles-per-row + 1);
}
</style>
