<template>
  <div id="app">
    <Header />
    <AddContact /><br><hr>
    <ViewContact />
  </div>
</template>

<script>
import Header from "./components/Header"
import AddContact from "./components/AddContact"
import ViewContact from "./components/ViewContacts"


export default {
  name: 'App',
  components: {
    Header,
    AddContact,
    ViewContact
  }
}
</script>

<style>
    * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background: #111111;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
</style>
