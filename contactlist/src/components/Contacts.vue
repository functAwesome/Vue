<template>
  <div id="Contacts">
      <h3>{{contacts.name}}</h3>
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
    .contacts {
        background:#f4f4f4;
        padding:10px;
        border-bottom:1px #ccc dotted;
    }
    .del {
        background: #ff0000;
        color: #fff;
        padding :5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }
</style>