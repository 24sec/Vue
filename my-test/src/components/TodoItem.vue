<template>
  <li class="item" >
      <input type="checkbox" v-model="checked">
      <slot name="myitem" v-bind="{checked}"></slot>
  </li>
</template>

<script>
export default {
    data(){
        return {
        
            checked:false
        }
    }
}
</script>

<style scoped>
.item {
  color: red;
}
</style>
