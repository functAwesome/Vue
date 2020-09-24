<template>
    <div id="AddContact" class="centered">
        <form @submit="AddContact">
            <input type="text" v-model="nameandsurname" placeholder="Name and Surname"><br>
            <input type="text" v-model="cellnumber" placeholder="Cell Number"><br>
            <input type="submit" value="Save">
        </form>
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
        width: 100%;
        margin-top: 20vh;
        display: inline-block;
        align-items: center;
    }
    form {
        text-align: center;
    }
    input {
        text-align: center;
        margin: 20px;
        font-size: 18px;
        width: 20em;
        height: 4em;
        color: #222222;
        border:none;
        background-color: rgba(181, 188, 165, 0.3);
    }
    hr {
        width: 20em;
        height: 1px;
        background: #384262 !important;
        border:none;
    }
</style>