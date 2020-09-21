<template>
  <div id="ViewContact">
      <div v-bind:key="contact.id" v-for="contact in contacts">
          <Contacts v-bind:Contacts="Contacts"/>
      </div>
  </div>
</template>

<script>
import Contacts from "./Contacts.vue"



export default {
  name: 'ViewContact',
  props:["contacts"],
  components: {
    Contacts
  },
  

}
</script>

<style>

</style>