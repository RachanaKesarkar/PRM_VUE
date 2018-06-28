<template>
  <div>
    <show-blog></show-blog>
  </div>
  
</template>

<script>
import addBlog from './components/addBlog.vue';
import showBlog from './components/showBlog.vue';

export default {
  components: {
    'add-blog': addBlog,
    'show-blog': showBlog
  },
  data () {
    
    return {
      
    }
  }
}

</script>

<style>

</style>
