<template>
    <div v-if="age >= 18">
        <h1> Welcome {{ name }}</h1>
    </div>
    <div v-else>
        <h1> Maaf kamu belum cukup umur </h1>
    </div>
    <button @click="greet">Sapa</button>
</template>

<script>
import MyComponent from './MyComponent.vue';

export default {
    props: ['name', 'age'],
    components :{
       MyComponent 
    }, methods : {
        greet() {
            alert("Halo Andika")
        }
    }
}
</script>