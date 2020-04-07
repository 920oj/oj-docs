<template>
  <div class="header-wrapper">
    <div class="header">
      <h1 class="header-title">{{title}}</h1>
      <p>by 920OJ</p>
      <p class="header-date">最終更新日: {{date}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    'title',
    'date'
  ]

}
</script>

<style scoped>

.header-wrapper {
  width: 100%;
  background: url('~static/img/bg/bg.jpg');
  background-size: cover;
  display :flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.header {
  display :flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 90%;
  margin: 0 auto;
}

.header-title {
  font-size: 2.2rem;
  font-weight: 400;
  line-height: 1.5;
  margin: 3rem 0 0.2rem 0;
  text-align: center;
}

.header p {
  color: #707070;
}

.header-date {
  margin: 2rem;
  font-size: 0.8rem;
}

@media screen and (max-width: 700px) {
  .header-title {
    font-size: 1.5rem;
  }
}

@media screen and (max-width: 500px) {
  .header-title {
    font-size: 1.2rem;
  }
}

</style>