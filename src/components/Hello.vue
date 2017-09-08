<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <hr>
    <h1>{{ message }}</h1>
    <p>Jin test 1: Learning Vue info..</p>
    <div>
      <ul>
        <li><a href="https://vuejs.org/v2/guide/">More info on Vue</a>&nbsp;&nbsp;&raquo;</li>
        <li><a href="https://vuejs.org/v2/guide/syntax.html">More info on Vue templates</a>&nbsp;&nbsp;&raquo;</li>
      </ul>
    </div>
    <br>

    <p>Jin test 2: Count Up and Down eg.</p>
    <div>
      <h2>You are a <strong>{{level}}</strong></h2>
      <p> current count: {{count}}</p>
      <button v-on:click="countUp" class="btn btn-primary">Count Up</button>
      <button @click="countDown" class="btn btn-primary">Count Down</button>
    </div>
    <br>
    <hr>

    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
      <br>
      <li><a href="http://vuejs-templates.github.io/webpack/" target="_blank">Docs for This Template</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App. This is a test from salperri',
      message: '& test from Jin...',
      count: 10,

    }
  },

  methods: {
    countUp: function() {
      this.count += 10;
    },

    countDown: function() {
      this.count -= 10;
    },

  },

  computed: {
      level: function() {
        if (this.count >= 200) {
          return "Pro";
        } else if (this.count >= 100) {
          return "Intermediate";
        } else if (this.count >= 0) {
          return "Beginner";
        } else {
          return "Banned";
        }
      },
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
