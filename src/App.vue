<script>

export default {
  name: "App",
  data(){ 
    return {
      greet: "Hello",
      name: "Batman",
      channel: "<b>Codevolution</b>",
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a Prize!</a>`,
      headingId: "heading",
      isDisabled: false
    };
  }
}

</script>

<template>
  <div>
    <!-- <div>{{ greet }} {{ name }}</div>
    <div v-text="channel"></div> -->
    <!-- <div v-text="name">Hello</div> -->

    <div v-html="channel"></div>
    <div v-html="hack"></div>
    <!-- <div>{{ hack }}</div> -->

    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">Bind</button>
  </div>
</template>

<style scoped>
</style>
