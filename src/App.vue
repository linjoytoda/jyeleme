<template>
  <div id="app">
    <v-header :seller="seller"></v-header>
    <v-tab></v-tab>
    <router-view :seller="seller"></router-view>
  </div>
</template>

<script>
import Header from './components/header/header'
import Tab from './components/tab/tab'

const ERR_OK=0

export default {
  name: 'app',
  data(){
    return{
      seller:{}
    }
  },
  created(){
    this.$http.get('/api/seller').then(response => {
      if(response.body.err===ERR_OK){
        this.seller=response.body.data
      }
    })
  },
  components: {
    "v-header":Header,
    "v-tab":Tab
  }
}
</script>

<style>

</style>
