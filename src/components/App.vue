<template>
  <div id="app">
    Got jokes?
    <button class="btn btn-primary" @click="initJokes">Add Ten random jokes</button>
    <div>
      {{$store.state}}
    </div>
  </div>  
</template>
<script>
import { mapActions } from 'vuex'
export default {
  methods: mapActions([
    'initJokes'
  ])
}
</script>
