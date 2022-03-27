<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" v-model="text">
    <input type="text" v-model="text2">
  </div>
</template>

<script>
export default {
  name: 'About',
  props: {
    msg: String
  },
  data () {
    return {
      text: '',
      text2: ''
    }
  },
  mounted () {
    this.getData()
  },
  methods: {
    getData () {
      this.text = Math.random().toString().substring(2)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
