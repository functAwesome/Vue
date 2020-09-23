<template>
    <div class="container">
        <div id="EditContact" class="centered">
            <form @submit="EditContact">
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
  name: 'EditContact',
  data(){
      return {
          id:'',
          nameandsurname: '',
          cellnumber:''
      }
  },
  props:["contact"],
  components: {
    
  },
  methods: {
      EditContact(e) {
        e.preventDefault();
        const SaveContact ={
            id:uuid(),
            name: this.nameandsurname,
            cellnumber: this.cellnumber
        }
        this.$emit('save-contact', SaveContact);
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
