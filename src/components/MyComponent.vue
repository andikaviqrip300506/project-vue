<template>
    <div>
        <h2> Nama : {{ nama }} </h2>
        <h2> Umur : {{ umur }} </h2>
    </div>
</template>

<script>
export default {
    name: "MyComponent",
    props: ['nama', 'umur'],
    data() {
        return {
            message: "Ini pesan dari komponen"
        }
    }, methods: {
        greet() {
            console.log("Hi!")
        }
    },
}
</script>

<style>
h1 {
    color:burlywood;
    text-align: left;
}

p {
    size: 16px;
    text-align: left;
}
</style>