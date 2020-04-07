<template>
  <div class="article">
    <Header :title="content.title" :date="content.updatedAt" />
    <Contents :text="content.contents" />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Contents from '~/components/Contents.vue';
import Footer from '~/components/Footer.vue';

export default {
  head() {
    return {
      title: this.content.title + ' | OJのドキュメント置き場',
      meta: [
        { hid: 'description', name: 'description', content: this.content.description },
        { hid: 'og:title', name: 'og:title', content: 'OJのドキュメント置き場' },
        { hid: 'og:url', name: 'og:url', content: 'https://d.920oj.net/' + this.$route.name},
        { hid: 'og:type', name: 'og:type', content: 'website' },
        { hid: 'og:description', name: 'og:description', content: this.content.title + ' | OJのドキュメント置き場' },
        { hid: 'og:image', property: 'og:image', content: 'https://d.920oj.net/img/ogp.jpg' },
        { hid: 'twitter:card', name: 'twitter:card', content: 'summary_large_image' },
        { hid: 'og:site_name', property: 'og:site_name', content: 'OJのドキュメント置き場' },
        { hid: 'og:locale', property: 'og:locale', content: 'ja_JP' },
      ]
    }
  },
  components: {
    Header,
    Contents,
    Footer,
  },
  async asyncData({ app, params }) {
    const config = { 
      'X-API-KEY': process.env.API_KEY
    }
    const response = await app.$axios.$get(`https://ojdocs.microcms.io/api/v1/docs/${params.id}`, { headers: config });
    return {
      content: response
    }
  }
}
</script>

<style>

</style>