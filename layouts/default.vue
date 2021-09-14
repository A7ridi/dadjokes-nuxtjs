<template>
  <div class="container">
    <LoadingBar v-if="showHideSpinner" />
    <AppHeader />
    <nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader'
import LoadingBar from '../components/LoadingBar'

export default {
  components: {
    AppHeader,
    LoadingBar,
  },
  beforeCreate() {
    this.showHideSpinner = true
  },
  mounted() {
    this.showHideSpinner = false
  },
  data() {
    return {
      showHideSpinner: true,
    }
  },
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  background: #f4f4f4;
}
a {
  color: #666;
  text-decoration: none;
}
ul {
  list-style: none;
}
.container {
  max-width: 800px;
  margin: 2rem auto;
  overflow: hidden;
  padding: 1rem 2rem;
  background: #fff;
}
</style>
