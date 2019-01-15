<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <router-link to='/b'>去B页面</router-link>
  </div>
</template>

<script>
export default {
  name: "aaa",
  data() {
    return {
      msg: "aaaaa"
    };
  },
  created() {
    this.name();
  },
  methods: {
    name() {
      function buy() {
        return new Promise((resolve, reject) => {
          setTimeout(() => {
            if (Math.random() < 0.5) {
              resolve("mai");
            } else {
              reject("err");
            }
          }, Math.random() * 10000);
        });
      }
      buy().then(
        data => {
          console.log(data);
        },
        err => {
          console.log(err);
        }
      );
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
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
