<template>
  <div id="ViewContact">
    <hr>
    <div v-bind:key="Contact.id" v-for="Contact in Contacts">
        <Contacts 
        v-bind:Contacts="Contact" 
        v-on:del-contact="$emit('del-contact', Contact.id)" 
        v-on:edit-contact="$emit('edit-contact', Contact.id)" 
        />
    </div>
  </div>
</template>

<script>
import Contacts from "./Contacts.vue"

export default {
  name: 'ViewContact',
  props:["Contacts"],
  components: {
    Contacts
  },

}
</script>

<style scoped>
hr {
  border:none;
  background: #384262 !important;
  height: 5px;
}
</style>