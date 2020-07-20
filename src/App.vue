<template>
  <div id="app">
    <form v-if="isSearch">
      <input ref="inputSearch" type="text" placeholder="search..." />
    </form>
    <button @click="onClickSearchToggle">검색하기</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      isSearch: false
    }
  },
  methods: {
    onClickSearchToggle () {
      this.isSearch = !this.isSearch
      this.$nextTick(() => this.$refs.inputSearch.focus())
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
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
</style>
