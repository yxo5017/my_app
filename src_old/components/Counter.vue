<template>
  <div>
    <button @click="increment">increment {{ step }}</button>
    <span>total {{ count }}</span>
  </div>
</template>

<script>
  export default {
    name: "Counter",
    computed: {
      step() { return this.$store.getters['counter/step']},
      count() { return this.$store.getters['counter/count']}
    },
    methods: {
      increment() {
        this.$store.dispatch('counter/increment')
      }
    }
  }
</script>

<style scoped>

</style>
