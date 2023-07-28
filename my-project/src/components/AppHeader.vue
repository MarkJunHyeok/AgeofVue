<script>
export default {
  props: ['propsData'],
  methods: {
    sendEvent() {
      this.$emit('renew')
    }
  }
}

</script>

<template>
  <header>
    <h1>{{propsData}}</h1>
    <button v-on:click="sendEvent">Send</button>
  </header>
</template>

<style>

</style>