<template>
  <div id="app">
    <Header />
    <EditContact v-if="isEdit" :contact="selectedContact" v-on:save-contact="SaveContact" />
    <AddContact v-else v-on:add-contact="AddContact" />
    <ViewContacts v-bind:Contacts="Contacts" v-on:del-contact="DeleteContact" v-on:edit-contact="EditContact" />
  </div>
</template>

<script>
import Header from "./components/Header"
import AddContact from "./components/AddContact"
import ViewContacts from "./components/ViewContacts"
import EditContact from "./components/EditContact"


export default {
  name: 'App',
  components: {
    Header,
    AddContact,
    ViewContacts,
    EditContact
  },
  data() {
    return{
      isEdit: false,
      selectedContact: '',
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
    DeleteContact(id) {
      this.Contacts = this.Contacts.filter(Contacts => Contacts.id != id);
    },
    AddContact(NewContact) {
      this.Contacts = [...this.Contacts, NewContact];
    },
    EditContact(id) {
      this.selectedContact = id
      this.isEdit = true
    },
    SaveContact(SaveContact) {
      let i = this.Contacts.findIndex(e => e.id == this.selectedContact)

      console.log(this.Contacts)
      this.Contacts[i].id = SaveContact.id
      this.Contacts[i].name = SaveContact.name
      this.Contacts[i].cellnumber = SaveContact.cellnumber
      console.log(this.Contacts)
    }
  }
}
</script>

<style>
    * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    background: #222222;
    color: aliceblue;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
  hr {
        height: 1px;
        background: #B5BCA5 !important;
        border:none;
    }
  ViewContacts {
    margin-top: 8%;
  }
</style>

