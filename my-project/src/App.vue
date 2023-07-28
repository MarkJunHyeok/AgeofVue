<script>
import AppHeader from "@/components/AppHeader.vue";
export default {
  data() {
    return {
      str: 'Header'
    }
  },
  components: {
    AppHeader
  },
  methods: {
    renewString() {
      this.str = 'RENEW'
    }
  }
}
</script>

<template>
  <div>
    <AppHeader
        v-bind:props-data="str"
        v-on:renew="renewString"
    />
    {{ str }}
  </div>
</template>

<style>

</style>