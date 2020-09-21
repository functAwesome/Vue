<template>
  <div id="app">
    <Header />
    <AddContact /><br><hr>
    <ViewContacts v-bind:Contacts="Contacts"/>
  </div>
</template>

<script>
import Header from "./components/Header"
import AddContact from "./components/AddContact"
import ViewContacts from "./components/ViewContacts"


export default {
  name: 'App',
  components: {
    Header,
    AddContact,
    ViewContacts
  },
  data() {
    return{
      Contacts: [
        {
        id: 1,
        name: "John",
        surname: "Doe",
        cellnumber: "0653310799"
      },
      {
        id: 2,
        name: "Sally",
        surname: "Doe",
        cellnumber: "0653318819"
      },
      {
        id: 3,
        name: "Marge",
        surname: "Doe",
        cellnumber: "0765513746"
      }
      ]
    }
  }
}
</script>

<style>
    * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background: #111111;
    color: aliceblue;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
</style>
