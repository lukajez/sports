<template>
  <div class="headlines"></div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      matchMoments: null,
    };
  },
  mounted() {
    const axios = require("axios");
    axios
      .get("http://192.168.15.17:8000/api/moments/")
      .then((res) => {
        this.matchMoments = res;
        console.log(this.matchMoments);
      })
      .catch((err) => {
        console.log(err);
      });
  },
  //   methods: {
  //       getHeadlinesFromApi() {
  //           return ;
  //       }
  //   }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
