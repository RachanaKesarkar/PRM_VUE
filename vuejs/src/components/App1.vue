<template>
  <div>
        <app-header></app-header>
        <app-test v-bind:ninjas="ninjas"></app-test>
        <app-footer></app-footer>
  </div>
  
</template>

<script>

import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Test from './components/Test.vue';

export default {
  components:{
    'app-header': Header,
    'app-footer': Footer,
    'app-test': Test
  },
  data () {
    return {
      ninjas: [
            {name:'First', speciality:'Vue Component', show: false},
            {name:'Second', speciality:'HTML Wizard', show: false},
            {name:'Third', speciality:'Click Events', show: false},
            {name:'Forth', speciality:'Conditionals', show: false},
            {name:'Fifth', speciality:'Web Pack', show: false},
            {name:'Sixth', speciality:'Data Diggin', show: false}
      ]
    }
  }
}
</script>

<style>

</style>
