<template>
    <div class="container">
        <div id="EditContact" class="centered">
            <h1>Edit an existing contact:</h1>
            <form @submit="EditContact">
                <input type="text" v-model="nameandsurname" placeholder="Name and Surname"><hr>
                <input type="text" v-model="cellnumber" placeholder="Cell Number"><hr>
                <input type="submit" value="Save">
            </form>
        </div>
    </div>
</template>

<script>

export default {
  name: 'EditContact',
  data(){
      return {
          nameandsurname: '',
          cellnumber:''
      }
  },
  props:["contacts"],
  components: {
    
  },
  methods: {
      EditContact(e) {
        e.preventDefault();
        const EditedContact ={
            id: this.contact.id,
            name: this.nameandsurname,
            cellnumber: this.cellnumber
        }
        this.$emit('save-contact', EditedContact);
    }
  }
}
</script>

<style scoped>
    
    #EditContact {
        margin-left: auto;
        margin-right: auto;
        margin-top: 11vh;
        display: inline-block;
        align-items: center;
    }
    input {
        text-align: center;
        margin: 20px;
        font-size: 18px;
        width: 20em;
        height: 4em;
        color: #A0D2Eb;
    }
</style>
