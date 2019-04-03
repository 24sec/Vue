<template>
  <div id="app">
    {{msg}}
    <input type="text" v-model="info">
    <button @click="add">添加</button>
    <ul>
      <todo-item :key="val" v-for="val in list">
        <template v-slot:myitem="itemProps">
          <span :style="{fontSize:'50px',color:itemProps.checked?'red':'blue'}">{{val}}</span>
        </template>        
        
      </todo-item>
    </ul>
    
  </div>
  
</template>

<script>
import TodoItem from './components/TodoItem.vue'
export default {
  name: 'app',
  components: {
    TodoItem
  },
  data(){
    return {
      msg:'hello world',
      info:'',
      list:[]
    }
  },
  methods:{
    add(){
      this.list.push(this.info);
      this.info='';
    }
  }
}
</script>

<style>

</style>
