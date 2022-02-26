<template>
  <div class="hello">
    <h1>Hello World {{ message }}</h1>
  </div>
</template>

<script>
import { axios } from "/app/plugins/axios";

export default {
  components: {},
  data() {
    return {
      message: "",
    };
  },
  mounted() {
    //get_hoge()の実行結果を変数messageに渡す
    this.get_hoge().then((response) => {
      this.message = response.data.message;
    });
  },
  methods: {
    //FastAPI(http://localhost:3000/api/hoge)にgetをリクエスト
    get_hoge() {
      return axios.get("api/fuga");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>

