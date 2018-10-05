<template>
  <div class="header">
    <nav class="nav-menu">
      <ul class="nav-menu-list">
        <li><a href="#">home</a></li>
        <li><a href="#">about us</a></li>
        <li><a href="#">contact us</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: black;
  text-decoration: none;
}
.header {
  position: -webkit-sticky;
  position: sticky;
  top: 30px;
  z-index: 9;
}
.nav-menu-list a:hover {
  text-decoration: underline;
}

</style>
