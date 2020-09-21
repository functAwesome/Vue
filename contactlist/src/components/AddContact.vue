<template>
  <div id="AddContact">
      <form>
          <input type="text" placeholder="Name and Surname"><hr>
          <input type="text" placeholder="Cell Number"><hr>
          <input type="button" value="Add Contact">
      </form>
  </div>
</template>

<script>


export default {
  name: 'AddContact',
  components: {
    
  }
}
</script>

<style scoped>
    #AddContact {
        display: inline-block;
        padding-left: 38.9%;
    }
    input {
        text-align: center;
        margin: 20px;
        font-size: 18px;
        width: 20em;
        height: 4em;
        color: #A0D2Eb;
    }
</style>