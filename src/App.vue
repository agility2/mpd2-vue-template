<template>
  <topSection :pageInfo="pageInfo[0].topSection[0]"/>
  <otherSection :pageInfo="pageInfo[0].otherSection[0]"/>
</template>

<script>
import topSection from './components/topSection.vue';
import otherSection from './components/otherSection.vue';

import axios from 'axios'
export default {
  name: 'App',
  components: {
    topSection,
    otherSection
  },
  data() {
   return {
     pageInfo: null
   }
  },
    created() {
     //Get json file from the page name we will have to rename this folder 
    axios.get('/dswaves/pageName/main.json').then((response) => {
        this.pageInfo = response.data
    });        
  }
}
</script>
