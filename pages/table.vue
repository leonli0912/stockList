<template>
    <div id="app">
 <div id="table-wrapper" class="ui container">
    <vuetable ref="vuetable"
    api-url="http://stocktest.hronyun.cn/allDividend?year=2019"
    :fields="['stockId','reportYear','dividendDate','divdendContent']"
    data-path=""
    pagination-path=""
    
    >
    </vuetable>
    <v-data-table dense :headers="headers" :items="desserts" item-key="name" class="elevation-1">
      </div>
</div>
</template>

<script>
import Vuetable from 'vuetable-2'
import vuetify from 'vuetify'

function setState(store) {}

export default {
    name: 'table',
    components:{
        Vuetable
    },
    data(){
        return{

    desserts: [
      {
        name: 'Frozen Yogurt',
        calories: 159,
        fat: 6.0,
        carbs: 24,
        protein: 4.0,
        iron: '1%',
      },
      {
        name: 'Ice cream sandwich',
        calories: 237,
        fat: 9.0,
        carbs: 37,
        protein: 4.3,
        iron: '1%',
      },
      {
        name: 'Eclair',
        calories: 262,
        fat: 16.0,
        carbs: 23,
        protein: 6.0,
        iron: '7%',
      },
      {
        name: 'Cupcake',
        calories: 305,
        fat: 3.7,
        carbs: 67,
        protein: 4.3,
        iron: '8%',
      },
      {
        name: 'Gingerbread',
        calories: 356,
        fat: 16.0,
        carbs: 49,
        protein: 3.9,
        iron: '16%',
      },
      {
        name: 'Jelly bean',
        calories: 375,
        fat: 0.0,
        carbs: 94,
        protein: 0.0,
        iron: '0%',
      },
      {
        name: 'Lollipop',
        calories: 392,
        fat: 0.2,
        carbs: 98,
        protein: 0,
        iron: '2%',
      },
      {
        name: 'Honeycomb',
        calories: 408,
        fat: 3.2,
        carbs: 87,
        protein: 6.5,
        iron: '45%',
      },
      {
        name: 'Donut',
        calories: 452,
        fat: 25.0,
        carbs: 51,
        protein: 4.9,
        iron: '22%',
      },
      {
        name: 'KitKat',
        calories: 518,
        fat: 26.0,
        carbs: 65,
        protein: 7,
        iron: '6%',
      },
    ],
    headers: [
      {
        text: 'Dessert (100g serving)',
        align: 'left',
        sortable: false,
        value: 'name',
      },
      { text: 'Calories', value: 'calories' },
      { text: 'Fat (g)', value: 'fat' },
      { text: 'Carbs (g)', value: 'carbs' },
      { text: 'Protein (g)', value: 'protein' },
      { text: 'Iron (%)', value: 'iron' },
    ],
  
        }
            

    }
};
</script>

<style lang="stylus" scoped>
#app 
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  color: #2c3e50


.orange.glyphicon 
  color: orange


th.sortable 
  color: #ec971f


.page-index
    display flex
    justify-content center
    align-items center
    flex-direction column

    h2
        font-size 46px
        font-weight 500
        margin-bottom 0

</style>