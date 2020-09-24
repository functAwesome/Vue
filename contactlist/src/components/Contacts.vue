<template>
  <div id="Contacts">
    <h3>Name: {{Contacts.name}}  <br>Cell Number: {{Contacts.cellnumber}}</h3> 
    <input class="edit-but" type="button" @click="$emit('edit-contact', Contacts.id)" value="Edit">
    <input class="del-but" type="button" @click="$emit('del-contact', Contacts.id)" value="X"> 
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
    background:#384262;
    padding:10px;
    margin-top: 10px;
    font-size: 20px;
    border-bottom:1px #ccc dotted;
    text-align: center;
    margin-left: 15%;
    margin-right: 15%;
  }
  .del {
    background: #ff0000;
    color: #000;
    padding :5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
  }
  .del-but{
    margin-top:5px;
    height: 30px;
    width: 30px;
    border-radius: 90%;
    background-color: red;
    border: none;
    color: #000;
    font-size: 1em;
    margin-left: 15px;
    margin-right: 15px;
  }
  .edit-but{
    border-radius: 10%;
    border: none;
    background-color: yellow;
    color: black;
    margin-top:5px;
    font-size: 1em;
    margin-left: 15px;
    margin-right: 15px;  
  }
</style>