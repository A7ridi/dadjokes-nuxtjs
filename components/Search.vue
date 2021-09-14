<template>
  <form @submit.prevent="onSubmit">
    <input
      type="text"
      v-model="text"
      placeholder="Search Jokes..."
      class="search"
    />
    <input type="submit" value="Search Jokes" class="submit" />
  </form>
</template>

<script>
export default {
  name: 'SearchJokes',
  data() {
    return {
      text: '',
    }
  },
  methods: {
    onSubmit() {
      this.$emit('search-text', this.text)
      // this.text = ''
    },
  },
}
</script>

<style>
.search {
  width: 80%;
  padding: 0.5rem;
  border-radius: 5px;
  border: 1px solid #444;
}
.submit {
  width: 19%;
  padding: 8px 0px;
  border-radius: 5px;
  border: 1px solid;
  cursor: pointer;
}
</style>
