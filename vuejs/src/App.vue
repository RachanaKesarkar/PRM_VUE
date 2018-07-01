<template>
  <div>
    <add-prm></add-prm>
  </div>
  
</template>

<script>
import addBlog from './components/addBlog.vue';
import showBlog from './components/showBlog.vue';
import addPrm from './components/addPrm.vue';

export default {
  components: {
    'add-blog': addBlog,
    'show-blog': showBlog,
    'add-prm': addPrm
  },
  data () {
    
    return {
      
    }
  }
}

</script>

<style>

</style>
