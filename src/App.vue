
<template>
  <div>
    <h1>Formulir</h1>
    <form @submit.prevent="submitorm">
      <label for="">Nama</label>
      <input class="{'is-invalid' : isInvalidName}" 
      type="text" name="nama" id="nama" v-model="kontak.nama">
      <div v-if = "isInvalidName" class="error-message">
      Nama Harus Di Isi !
    </div>
      <br>
      <label for="">Email</label>
      <input class="{'is-invalid' : isInvalidEmail}" 
      type="email" name="email" id="email" v-model="kontak.email">
      <div v-if = "isInvalidEmail" class="error-message">
       Email Harus Di Isi !
       </div>
      <br>
      <button type="submit">Simpan</button>
      <br>
    </form>
    <div v-if="showResult">
      nama : {{ name }} <br>
      email : {{ email }}
    </div>
  </div>
</template>

<script>
  
import { ref } from 'vue';
export default {
  name: 'MyComponent',
  data() {
    return {
       kontak : 
        {
          nama: '', 
          email: ''
        },
      showResult: ref(false),
      name: ref(''),
      email: ref(''),
      };
    },
    computed : {
      isInvalidName() {
        return this.kontak.nama.length < 1 ;
      },
      isInvalidEmail() {
        return this.kontak.email.length < 1 ;
      }
    },
      methods: {
        submitorm() {
      this.name = this.kontak.nama; 
      this.email = this.kontak.email;
      this.showResult = true;
      this.isInvalidName = false;
      this.isInvalidEmail = false
         
      }
     }
    }
  
     
     
</script>

<style>
h1 {
  color: blue;
}

.error-message{
  color:red;
  margin-top: 5px
}

.is-invalid {
  border-color:red;
}
</style>