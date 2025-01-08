<script>

export default {
  name: "App",
  data(){ 
    return {
      greet: "Hello",
      name: "Batman",
      channel: "<b>Codevolution</b>",
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a Prize!</a>`
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
  </div>
</template>

<style scoped>

</style>
