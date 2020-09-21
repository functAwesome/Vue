<template>
  <div id="ViewContact">
      <div v-bind:key="Contact.id" v-for="Contact in Contacts">
          <Contacts v-bind:Contacts="Contacts"/>
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

<style>

</style>