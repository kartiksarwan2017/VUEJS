<template>
    <div>
        <!-- <h2 v-if="num === 0">The number is zero</h2>
        <h2 v-else-if="num < 0">The Number is Negative.</h2>
        <h2 v-else-if="num > 0">The Number is Positive.</h2>
        <h2 v-else>Not a Number</h2> -->
    
        <!-- <div v-if="display === true">
            <h2>Krishna</h2>
            <h2>Codeevolution</h2>
            <h2>Vue</h2>
        </div> -->


        <!-- <template v-if="display === true">
            <h2>Krishna</h2>
            <h2>Codeevolution</h2>
            <h2>Vue</h2>
        </template>

        <h2 v-show="showElement">Using v-show</h2>
        <h2 v-if="showElement">Using v-show</h2> -->


        <!-- lIst rendering -->
         <!-- <h2 v-for="(name, index) in names" :key="index">{{ index }}  {{ name }}</h2> -->

         <!-- <h2 v-for="(name, index) in fullNames" :key="index">{{ name.first }}  {{ name.last }}</h2>

         <div v-for="(actor, index) in actors" :key="index">
            <h2>{{actor.name}}</h2>
            <h3 v-for="movie in actor.movies" :key="movie">
                {{ movie }}
            </h3>
         </div>


         <h2 v-for="(value, key, index) in myInfo" :key="index">{{ index }} {{ key }}  {{value}}</h2> -->
         
         <!-- <template v-for="(name, index) in names" :key="index">
            <h2>{{ name }}</h2>
            <hr />
         </template> -->

         <!-- <h2 v-for="name in names" :key="name" v-if="name === 'Bruce'">{{ name }}</h2> -->

         <!-- <template v-for="name in names" :key="name">
            <h2 v-if="name === 'Bruce'">{{ name }}</h2>
         </template> -->


    </div>
</template>

<script>

export default {
    name: "ConditionalRendering",
    data() {
        return {
            num: 5,
            display: true,
            showElement: false,
            names: ['Bruce', 'Clark', 'Diana'],
            fullNames: [
                { first: "Bruce", last: "wayne" },
                { first: "Clark", last: "Kent" },
                { first: "Princess", last: "Diana" }
            ],
            actors: [
                {
                name: "Christain Blae",
                movies: ["Batman", "The Prestige"]
                }, 
                {
                    name: "Di Caprio",
                    movies: ["titanic", "Incpetion"]
                }
            ],
            myInfo: {
                name: "Krishna",
                channel:"Vue 3"
            }
        }
    }
}
</script>

<style></style>
