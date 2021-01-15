<template>
<div class="dsw-container dsw-mx-auto">

    <!-- Test of how to bring in the content from JSON file to a specific component -->
     {{ pageInfo.test2 }} 


</div>
</template>
<script>
export default {
    props:['pageInfo'],
    name: 'Page',
  data() {
    return {
      data: '',
      msg: 'Hello World'
    }
  },
  mounted() {

  },
  computed: {
    
  },
  methods: {    

  }
}
</script>