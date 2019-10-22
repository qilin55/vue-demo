<template>
  <div class="hello">
    <p>{{ message }}</p>
    <p>{{ reversedMessage }}</p>
    <button v-on:click="reverseMessage">反转消息</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data:()=>{
    return {
      message: 'hello coby'
    }
  },
  props: {
    msg: String
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  },
  computed: {
    // 计算属性的 getter
    reversedMessage: function () {
      // `this` 指向 vm 实例
      return this.message.split('').reverse().join('')
    }
  }
}
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
