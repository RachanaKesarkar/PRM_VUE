<template>
  <div>
    <h1>List of ninja</h1>
    <ul>
        <li v-for="ninja in ninjas"> {{ ninja }}</li>
    </ul>
  </div>
  
</template>

<script>
export default {
  data () {
    return {
      ninjas: ['First', 'Second', 'Third']
    }
  }
}
</script>

<style>
h1{
    color: green;
  }
</style>
