<template>
  <div id="ViewContact">
      <Contacts />
      <RemoveContact />
      <EditContact />
  </div>
</template>

<script>
import Contacts from "./Contacts"
import RemoveContact from "./RemoveContact"
import EditContact from "./RemoveContact"




export default {
  name: 'ViewContact',
  components: {
    Contacts,
    RemoveContact,
    EditContact
  }
}
</script>

<style>

</style>