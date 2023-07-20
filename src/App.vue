<script setup>
import { ref } from 'vue'

const msg = "<h1> Hai </h1>" // Harus memakai rawHTML
const hai = "hai" // Bisa menggunakan {{ hai }}
const link = "https://www.google.com/url?sa=i&url=https%3A%2F%2Fepaper.mediaindonesia.com%2Fdetail%2Fmonyet-juga-menyapa-seperti-manusia&psig=AOvVaw10nWkOSJ_HI6_E-BxvRJgt&ust=1689922775160000&source=images&cd=vfe&opi=89978449&ved=0CA4QjRxqFwoTCODplo_bnIADFQAAAAAdAAAAABAI"
const number = prompt("")
const objek = {
  id : 'container',
  class : 'wrapper'
}
</script>

<template>
  <div :="objek">
   <h1 v-html="msg"></h1> 
   <h1> {{ hai }} </h1>
   <a :href="link"> Klik </a>
   <button :disabled="IsButtonDisabled"><a :href="link">Button</a></button>
   <p v-if="seen"></p>
   <p> {{ parseInt(number) }} </p>
   <p> {{ number ? 'TRUE : 1' : 'FALSE : 0' }}</p>

   
  </div>
</template>