<template>
  <div class="hello">
    <h1>hogehoge {{ message }}</h1>
  </div>
</template>

<script>

import { axios } from '/app/plugins/axios'

export default {
    components: {
    },
    data() {
      return {
        message : ''
      }
    },
    mounted() {
      this.get_hello().then((response) =>{
        this.message = response.data.message
      })
    },
    methods: {
      get_hello() {
        return axios.get('api/hoge')
      }
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>

