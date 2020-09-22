<template>
  <div id="Contacts">
      <h3>Name: {{Contacts.name}}  <br>Cell Number: {{Contacts.cellnumber}}</h3> 
      <input type="button" @click="$emit('del-contact', Contacts.id)" value="Delete"> 
      <input type="button" @click="$emit('edit-contact', Contacts.id)" value="Edit">
  </div>
</template>

<script>


export default {
  name: 'Contacts',
  components: {
    
  },
  props:["Contacts"]
}
</script>

<style>
    #Contacts {
        background:#f4f4f4;
        padding:10px;
        margin-top: 10px;
        font-size: 20px;
        border-bottom:1px #ccc dotted;
        text-align: center;
    }
    .del {
        background: #ff0000;
        color: #000;
        padding :5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>