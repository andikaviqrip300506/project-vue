<template>
    <div>
        <h2 v-if="umur >= 18"> {{ pesanSelamat }}</h2>
        <p v-else> maaf, kamu belum cukup umur</p>
        <button @click="greet">Sapa Bro</button>
    </div>
</template>

<script>
export default {
    props: ['nama', 'umur'],
    data() {
        return {
            pesan: 'halo, ' + this.nama + '!'
        }
    }, methods: {
        greet() {
            console.log('halo bro !')
        }
    },
    computed: {
        pesanSelamat() {
            return "Selamat Siang" + this.nama + '!';
        }
    },
    watch: {
        umur(newUmur, oldUmur) {
            console.log('Umur berubah dari', oldUmur, 'Menjadi', newUmur)
        }
    }
}
</script>