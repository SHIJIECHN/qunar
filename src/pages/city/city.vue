<template>
  <div>
    <city-header></city-header>
    <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/Header.vue'
import CityList from './components/List.vue'

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
}
</script>
<style scoped>
</style>