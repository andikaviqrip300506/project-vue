<template>
    <div>
        <input type="text" v-model="cari" placeholder="Cari Data">
        <ul>
            <li v-for="item in cariData" :key="item.id">
            {{ item.title }} - {{ item.price }}
            </li>
            <p v-if="cariData.length ===  0"> barang tidak tersedia </p>
        </ul>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            cari : '',
            product : []
        }
    },
    created() {
        this.product = [
            { id: 1, title:"Baju anak", price: 25000 },
            { id: 2, title:"Susu anak", price: 75000 },
            { id: 3, title:"Topi", price: 10000 },
            { id: 4, title:"Balon", price: 1000 },
            { id: 5, title:"Kinder joy", price: 15000 }
        ]
    },
    computed: {
        cariData() {
            return this.product.filter (( item ) => {
                return item.title.match(this.cari)
            })
        }
    }
}
</script>