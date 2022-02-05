<template>
<div>
  <navbar>
  </navbar>
  <div class="home-container">
    <home-page>
    </home-page>
</div>
<div class="stocks-container">
  <stocks-page>
  </stocks-page>
</div>
<div class="form-container">
  <form-page>
  </form-page>
</div>
<Footer></Footer>
</div>
</template>

<script>
import Navbar from './Navbar.vue'
import HomePage from './HomeScreen.vue'
import FormPage from './FormPage.vue'
import StocksPage from './StocksPage.vue'
import Footer from './Footer.vue'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    FormPage,
    StocksPage,
    HomePage,
    Footer,
    Navbar
  }

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
  color: #42b983;
}

.form-container {
  background-color: rgb(189, 189, 189);
}
</style>
