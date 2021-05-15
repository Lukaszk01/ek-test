<template>
  <div>
    <form @submit.prevent="emitQuery">
      <label for="search-form__input">Pick a TV show you like!</label>
      <input
        id="search-form__input"
        type="search"
        autocomplete="off"
        v-model="query"
      />
      <button @click="show = !show">Search</button>
    </form>
  </div>






  
</template>

<script>
export default {
  data() {
    return {
      show: false,
      query: this.getInitialQueryValue()
    };
  },
  watch: {
    $route() {
      this.query = this.getInitialQueryValue()
    }
  },
  methods: {
    getInitialQueryValue() {
      return this.$route.query.search || "";
    },
    emitQuery() {
      this.$emit("submit:query", this.query);
    }
  }
};
</script>
<style>
  .fade-enter-active,
.fade-leave-active {
  transition: opacity 0.9s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>