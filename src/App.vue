<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <input type="text" :value="inputValue" @input="inputValue = $event.target.value">
    <p>{{inputValue}}</p> -->
    <!-- <ContactList></ContactList> -->
    <ContactList >
      <h2 slot="title">Ini Slots title</h2>
      <p slot="text">paragraph slot</p>
    </ContactList>
    <!-- <p v-for="(user, index) in dataUsers" :key="index">{{user.name}}</p> -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import dataUsers from './assets/users.json'
import ContactList from './components/ContactList'

export default {
  name: 'app',
  created(){
    this.dataUsers = dataUsers
  },
  components: {
    HelloWorld,
    ContactList
  },
  data () {
    return {
      dataUsers: [],
      inputValue: 'value input'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
