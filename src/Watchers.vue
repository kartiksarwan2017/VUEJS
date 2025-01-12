<template>
    <div>
        <h2>Volume Tracker (0-20)</h2>
        <h2>Current Volume: {{ volume }}</h2>

        <div>
            <button @click="volume += 2">Increase</button>
            <button @click="volume -= 2">Decrease</button>
        </div>

        <input type="text" v-model="movie">
        <input type="text" v-model="movieInfo.title">
        <input type="text" v-model="movieInfo.actor">

        <!-- <div>
            <button @click="movieList.push('Woder Woman')">Add Movie</button>
        </div> -->


        <div>
            <button @click="movieList = movieList.concat(['Woder Woman'])">Add Movie</button>
        </div>
    </div>
</template>

<script>

export default {
    name: "Watchers",
    data() {
        return {
            volume: 0,
            movie: "Batman",
            movieInfo: {
                title: "",
                actor: ""
            },
            movieList: [
                "Batman", "Superman"
            ]
        }
    },
    methods: {},
    computed: {},
    watch: {
        volume(newValue, oldValue) {
            if(newValue > oldValue && newValue == 16) {
                alert(`Listening to a high volume for a long time may damage your hearing`);
            }
        },
        movie: {
            handler(newValue) {
                console.log(`Calling API wiht movie Name: ${newValue}`)
            },
            immediate: true
        },
        movieInfo: {
            handler(newValue) {
                console.log(`Calling API with movie title: ${newValue.title} and actor ${newValue.actor}`);
            },
            deep: true
        },
        movieList: {
            handler(newValue) {
                console.log(`Updated List ${newValue}`)
            },
            // deep: true
        }
    }
}

</script>

<style></style>