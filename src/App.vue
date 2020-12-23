<template>
  <div id="app">
    <user v-bind:values="values"/>
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
        values: {
            imglink: '../assets/70.jpg',
            nickname: 'romashka',
            name: 'Иванов Иван Иванович',
            adress: 'Москва, Юбилейная 50',
            email: 'coldrabbit48@example.com',
            phone: '+7-495-266-57-34'
        }
    }
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
