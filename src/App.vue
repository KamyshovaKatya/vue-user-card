<template>
  <div id="app">
    <user v-bind:values="values"/>
    <button v-on:click="getUserData()">Обновить</button>
  </div>
</template>

<script>
import user from './components/Component.vue'

export default {
  name: 'app',
  components: {
    user
  },
  data() {
    return {
        values: {}
    }
  },
  methods: {
        getUserData(){
            this.axios.get('http://37.77.104.246/users/getrandom.php')
                .then((response) => {
                    this.values = response.data;
            })
        }
  },
  mounted() {
    this.getUserData();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
