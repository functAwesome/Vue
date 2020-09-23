<template>
    <div class="container">
        <div id="AddContact" class="centered">
            <h1>Add a new contact:</h1>
            <form @submit="AddContact">
                <input type="text" v-model="nameandsurname" placeholder="Name and Surname"><hr>
                <input type="text" v-model="cellnumber" placeholder="Cell Number"><hr>
                <input type="submit" value="Save">
            </form>
        </div>
    </div>
</template>

<script>
import { v4 as uuid } from "uuid";

export default {
  name: 'AddContact',
  data(){
      return {
          nameandsurname: '',
          cellnumber:''
      }
  },
  components: {
    
  },
  methods: {
      AddContact(e) {
        e.preventDefault();
        const NewContact ={
            id: uuid(),
            name: this.nameandsurname,
            cellnumber: this.cellnumber
        }
        this.$emit('add-contact', NewContact);
    }
  }
}
</script>

<style scoped>
    
    #AddContact {
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