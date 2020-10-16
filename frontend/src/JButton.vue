<template>
    <button v-on:click="click">ADD</button>    
</template>
<script>
export default {
    name:"JButton",
    methods:{
        click: function(){
            this.$emit('input');
        }
    }
}
</script>
<style>
button {
  width: 120px;
  height: 40px;
  color: white;
  background-color: #55ACED;
  border: none;
  padding: 15px;
  cursor: pointer;
}
</style>