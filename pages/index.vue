<template>
  <div class="index">
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
  components: {
    Header,
    Contents,
    Footer,
  },
  async asyncData({ app }) {
    const config = { 
      'X-API-KEY': process.env.API_KEY
    }
    const response = await app.$axios.$get('https://ojdocs.microcms.io/api/v1/docs/GhMW5KLqH', { headers: config });
    return {
      content: response
    }
  }
}
</script>

<style>

</style>
