<template>
  <div>
    <AppHeader v-bind:header="computedStr" v-on:renew="renewCount"></AppHeader>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  data : function () { // 변수등이 들어갈 곳...
     return {
        str : "Header!!~",
        surfix: ""
     }
  },
  computed: { // data를 기반으로 validation이나... kotlin의 get property 등.. 추가작업을 해야할 떄 사용하는듯
    computedStr: function () {
       return this.str + this.surfix
    }
  },
  methods: { // 함수들을 여기에 선언
    renewCount: function(v) {
      this.surfix = v
    }
  }, 
  components: { // 붙일 컴포넌트들을 여기에 씀
    AppHeader
  }
}
</script>

<style>

</style>