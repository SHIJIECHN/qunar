<template>
  <div>
    <city-header></city-header>
    <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/Header.vue'
import CityList from './components/List.vue'
import axios from 'axios'

export default {
  name: 'City',
  components: {
    'city-header': CityHeader,
    'city-list': CityList
  },
  data () {
    return {
    };
  },
  methods:{
    getCityInfo(){
      axios.get('/api/city.json').then(res=>{
        this.getCityInfoSuccess();
      })
    }
  },
  mounted(){
    this.getCityInfo();
  }
}
</script>
<style scoped>
</style>