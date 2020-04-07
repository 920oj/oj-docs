<template>
  <div class="contents">
    <div class="main" v-html="$md.render(text)" />
  </div>
</template>

<script>
export default {
  props: [
    'text'
  ]

}
</script>

<style>
.contents {
  padding: 0 1rem;
  line-height: 200%;
}

h2 {
  font-weight: 600;
  font-size: 1.5rem;
  margin-top: 2rem;
  margin-bottom: 0.5rem;
}

h3 {
  font-weight: 600;
  font-size: 1.25rem;
  margin-top: 2rem;
  margin-bottom: 0.5rem;
}

p {
  margin: 0.5rem 0;
  max-width: 100%;
}

img {
  width: 100%;
  margin: 1rem 0;
}

@media screen and (min-width: 700px) {
  .contents {
    max-width: 700px;
    margin: 0 auto;
  }
}

</style>