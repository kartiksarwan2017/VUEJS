<template>
    <div>
        <h2 v-if="num === 0">The number is zero</h2>
        <h2 v-else-if="num < 0">The Number is Negative.</h2>
        <h2 v-else-if="num > 0">The Number is Positive.</h2>
        <h2 v-else>Not a Number</h2>
    
        <!-- <div v-if="display === true">
            <h2>Krishna</h2>
            <h2>Codeevolution</h2>
            <h2>Vue</h2>
        </div> -->


        <template v-if="display === true">
            <h2>Krishna</h2>
            <h2>Codeevolution</h2>
            <h2>Vue</h2>
        </template>

        <h2 v-show="showElement">Using v-show</h2>
        <h2 v-if="showElement">Using v-show</h2>
    </div>
</template>

<script>

export default {
    name: "ConditionalRendering",
    data() {
        return {
            num: 5,
            display: true,
            showElement: false
        }
    }
}
</script>

<style></style>
