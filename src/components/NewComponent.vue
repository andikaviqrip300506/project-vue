<template>
<events :nama="nama" :umur="umur" @greeted="onGreeted"></events>
<slot name="header"></slot>
<slot name="footer"></slot>
</template>



<script>
import { ref } from 'vue'
import Validate from './Validate.vue';
import MyComponent from './MyComponent.vue';
import Computed from './Computed.vue';
import Wacthers from './Wacthers.vue';
import Events from './Events.vue';
export default {
components: {
  MyComponent,
  Validate,
  Computed,
  Wacthers,
  Events
   }

 }

 const nama = ref('andika')
 const umur = ref('17')

 const onGreeted = () => {
  console.log('donnnn')
 };

</script>

<style>

</style>