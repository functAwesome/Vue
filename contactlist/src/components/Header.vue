<template>
  <div id="Header">
      <h1>My Contact List</h1>
  </div>
</template>

<script>


export default {
  name: 'Header',
  components: {
    
  }
}
</script>

<style scoped>
    h1 {
        position: fixed;
        top: 0px;
        font-size: 3em;
        background: #A0D2Eb;
        text-align: center;
    }
    #Header {
        width: 100%;
        height: 11vh;
        background: #A0D2Eb;
        color: #494D5F;
        text-align: center;
        padding: 10px;
        padding-top: 20px;
        padding-left: 40%;
    }
</style>