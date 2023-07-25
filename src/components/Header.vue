<template>
    <div>
        <h3> ini header {{ text }} </h3>
    </div>
</template>

<script>
export default {
    name: "header",
    props: ['text'],
    data() {
        return {
            message: "Ini pesan dari header"
        }
    }, methods: {
        greet() {
            console.log("Hi!")
        }
    },
}
</script>

<style>
h3 {
    color:rgb(22, 209, 147);
    text-align: center;
    
}


</style>