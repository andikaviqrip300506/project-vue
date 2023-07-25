<script>
export default {
    props: ['nama', 'umur'],
    data() {
        return {
            pesan: 'halo, ' + this.nama + '!'
        }
    }, methods: {
        greet() {
            console.log('halo bro !');
            this.$emit('greeted')
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