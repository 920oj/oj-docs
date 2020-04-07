<template>
  <div class="index">
    <Header :title="title" :date="updatedAt" />
  </div>
</template>

<script>
import Header from '~/components/Header.vue';
export default {
  data() {
    return {
      title: 'OJのドキュメント置き場について',
      updatedAt: new Date(),
    }
  },
  components: {
    Header,
  }

}
</script>

<style>

</style>
