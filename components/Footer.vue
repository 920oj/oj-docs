<template>
  <div class="footer">
    <div class="footer-link">
      <ul>
        <li><a href="https://920oj.net/" rel="noopener" target="_blank">920oj.net</a></li>
        <li><a href="https://twitter.com/920oj" rel="noopener" target="_blank">Twitter</a></li>
        <li><a href="https://github.com/920oj" rel="noopener" target="_blank">GitHub</a></li>
      </ul>
    </div>
    <div class="footer-copyright">
      <p>&copy;Junya Oiwa (@920OJ)</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.footer {
  background-color: #282828;
  color: #FFF;
  padding: 1rem 0;
  margin-top: 30px;
}

ul {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style-type: none;
}

li {
  margin: 0 1rem;
}

.footer-link {
  margin: 1rem 0;
  margin-bottom: 2rem;
}

.footer-link a {
  text-decoration: none;
  color: #FFF;
}

.footer-link a:visited {
  color: #FFF;
}

.footer-copyright {
  text-align: center;
  font-size: 0.8rem;
}

</style>