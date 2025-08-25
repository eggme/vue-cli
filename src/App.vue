<template>
  <div>
    <AppHeader v-bind:header="computedStr" v-on:renew="renewCount"></AppHeader>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  data : function () {
     return {
        str : "Header!!~",
        surfix: ""
     }
  },
  computed: {
    computedStr: function () {
       return this.str + this.surfix
    }
  },
  methods: {
    renewCount: function(v) {
      this.surfix = v
    }
  },
  components: {
    AppHeader
  }
}
</script>

<style>

</style>