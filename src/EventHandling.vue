<template>
   <div>
        <h2>{{name}}</h2>
        <div>
            <button @click="changeName($event), increment(1, $event)">Change Name</button>
        </div>

        <h2>{{ count }}</h2>
        <div>
            <button @click="increment(1, $event)">Increment</button>
            <button @click="increment(5)">Increment 5</button>
            <button @click="decrement(1)">Decrement</button>
            <button @click="decrement(5)">Decrement 5</button>

            <button @click="changeUserName">Check Event</button>
        </div>
   </div>
</template>

<script>
   export default {
    name: "EventHandling",
    data() {
        return {
            name: "Vishwas", 
            count: 0
        }
    }, 
    methods: {
        increment(num, event) {
            this.count += num;
            console.log("Event", event);
        },
        decrement(num, event) {
            this.count -= num;
            console.log("Event", event);
        },
        changeName(event) {
            console.log("Event", event);
            this.name="Batman";
        },
        changeUserName($event) {
            console.log("Event: ", $event);
        }
    }
   }
</script>

<style>
   
</style>

