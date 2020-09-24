<template>
  <div id="Header">
      <h1><div class="s1">M</div>Y <div class="s1">C</div>ONTACT <div class="s1">L</div>IST</h1>
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
      top: 0px;
      font-size: 3em;
      background: #384262;
      text-align: center;
    }
    #Header {
      position: fixed;
      width: 100%;
      height: 20vh;
      background: #384262;
      color: #494D5F;
      text-align: center;
      padding: 10px;
      padding-top: 20px;
      text-align: center;
    }
    .s1 {
      display: inline;
      font-size: 75px;
      background: #384262;
    }
</style>