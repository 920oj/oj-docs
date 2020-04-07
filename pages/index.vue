<template>
  <div class="index">
    <Header :title="title" :date="updatedAt" />
    <Contents :text="contents" />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Contents from '~/components/Contents.vue';
import Footer from '~/components/Footer.vue';

export default {
  data() {
    return {
      title: 'OJのドキュメント置き場について',
      updatedAt: new Date(),
      contents: "## はじめに\nこんにちは、おーじぇい(@920OJ)です。\n\nこの度、「OJのドキュメント置き場( [https://d.920oj.net/](http://d.920oj.net/) )を公開しました。これは、一通りまとまった文書を置いて公開できる、自分専用のドキュメントサイトです。各ドキュメントはmarkdownで執筆し、microCMSでコンテンツを配信しています。Nuxt.jsのSPAモードでサイトを構築し、メンテナンスコストを格段に下げた運用を目指しています。\n\n### GitHubレポジトリ\n\nGitHubレポジトリはこちらになります。\n\n[https://github.com/920oj/oj-docs](https://github.com/920oj/oj-docs)\n\n## おわりに\n\n画像埋め込みのテストに、この前旅行した河津の桜を貼っておきます。画像埋め込みにはimgurを利用しています。\n\n![](https://i.imgur.com/kwjMVf1.jpg)\n\nこれからもどうぞ宜しくお願い致します。🙏",

    }
  },
  components: {
    Header,
    Contents,
    Footer,
  }

}
</script>

<style>

</style>
