<template>
    <div>
        <h2>FullName: {{ firstName }} {{ lastName }}</h2>
        <h2>Computed Full Name: {{ fullName }}</h2>

        <button @click="changeFullName">Change Full Name</button>

        <!-- <h2>Total = {{ items.reduce((total, curr) => (total = total + curr.price), 0) }}</h2> -->

        <button @click="items.push({id: 4, title: 'Keyboard', price: 50});">Add Item</button>

        <h2>Computed Total = {{ total }}</h2>
        <h2>Method Total = {{ getTotal() }}</h2>

        <input type="text" v-model="country">

        <template v-for="(item, index) in items" :key="index">
            <h2 v-if="item.price > 100">{{ item.title }} {{ item.price }}</h2>
        </template>

        <template v-for="item in expensiveItems" :key="item.id">
            {{ item.title }}
            {{ item.price }}
        </template>

        
    </div>
</template>

<script>
   export default {
    data() {
        return {
            firstName: "Shri",
            lastName: "Krishna",
            items: [
                {
                    id: 1,
                    title: "TV",
                    price: 100
                },
                {
                    id: 2,
                    title: "Phone",
                    price: 200
                },
                {
                    id: 3,
                    title: "Laptop",
                    price: 300
                }
            ],
            country: ""
        }
    },
    methods: {
        getTotal() {
            console.log("getTotal Method");
            return this.items.reduce((total, curr) => (total = total + curr.price), 0);
        },
        changeFullName() {
            this.fullName = "Clark Kent";
        }
    },
    computed: {
        fullName: {
            get() {
                return `${this.firstName} ${this.lastName}`;
            },
            set(value) {
                const names = value.split(" ");
                this.firstName = names[0];
                this.lastName = names[1];
            }
        },
        total() {
            console.log("total computed property");
            return this.items.reduce((total, curr) => (total = total + curr.price), 0);
        },
         expensiveItems() {
            return this.items.filter((item) => item.price > 100);
         }
    }
   }
</script>

<style>
</style>