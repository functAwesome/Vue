<template>
  <div id="app">
    <Header />
    <AddContact /><br><hr>
    <ViewContacts v-bind:Contacts="Contacts" v-on:del-contact="deleteContact" />
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
        name: "John Doe",
        cellnumber: "0653310799"
      },
      {
        id: 2,
        name: "Sally Doe",
        cellnumber: "0653318819"
      },
      {
        id: 3,
        name: "Marge Simpson",
        cellnumber: "0765513746"
      }
      ]
    }
  },
  methods:{
    deleteContact(id){
      this.Contacts = this.Contacts.filter(Contacts => Contacts.id != id);
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
