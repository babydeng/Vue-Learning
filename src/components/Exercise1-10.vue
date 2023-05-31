<template>
  <div>
    <h1>Vue Lifecycle hooks</h1>
    <ul>
      <li v-for="(item, n) in list" :key="n">
      {{ item }}
      <button @click="deleteItem(item)">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default{
  data(){
    return{
      list: ['Apex Legends',
    'A Plague Tale: Innocence',
    'ART SQOOL',
    'Baba Is You',
    'Devil May Cry 5',
    'The Division 2',
    'Hypnospace Outlaw',
    'Katana ZERO',
    'testing unmounted hooks destory',
    'test'],
  }
},
beforeCreate() {
    alert('beforeCreate: data is static, thats it')
  },
created() {
    alert('created: data is reactive, but DOM not ready yet')
  },  
beforeMount() {
    alert('beforeMount: DOM is ready, but not visible yet')
  },
mounted() {
    alert('mounted: DOM is ready and visible')
  },
beforeUpdate() {
    alert('beforeUpdate: we know an update is about to happen, and have the data')
},
updated() {
    alert('updated: virtual DOM will update after you click OK')
},
beforeUnmount() {
  alert('beforeUnmount: about to blow up this component')
},
unmounted() {
  alert('unmounted: this component has been destroyed')
},

methods: {
  deleteItem(value){
    this.list =  this.list.filter(item => item !== value)
  }
}

}</script>