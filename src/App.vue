<template>
  <section class="app">
    <Header />
    <DadPic />
    <Display v-bind:joke="joke"/>
    <Button v-on:get-joke="getJoke"/>
  </section>
</template>

<script>
import Header from './components/Header'
import Display from './components/Display'
import Button from './components/Button'
import DadPic from './components/DadPic'

import axios from 'axios'

export default {
  name: 'App',
  components: {
    DadPic,
    Header,
    Display,
    Button,
  },
  data() {
    return {
      joke: {data: {joke: 'ready for a joke?'}}
    }
  },
  methods: {
    getJoke() {
      // console.log('get joke!')
      axios('https://icanhazdadjoke.com', {
        headers: {
          accept: 'application/json'
        }
      })
        .then(data => this.joke = data)
        .catch(err => console.error(err))
    }
  }
}
</script>

<style>
   * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
