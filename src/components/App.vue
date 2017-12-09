<template>
  <div id="app">
    <h3>Got jokes?</h3>
    <button class="btn btn-primary" @click="initJokes">Add ten random jokes</button>
    <button class="btn btn-secondary" @click="addJoke">Add random joke</button>
    <br>
    <br>
    <div class="col-md-12">
      <Joke  
        v-for="(joke, index) in $store.state.jokes"
        :key="index"
        :joke ="joke"
      />
    </div>
  </div>  
</template>
<script>
import { mapActions } from 'vuex'
import Joke from './Joke.vue'
export default {
  methods: mapActions([
    'initJokes',
    'addJoke'
  ]),
  components: {
    Joke
  }
}
</script>
