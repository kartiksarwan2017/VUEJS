<script>

// import ConditionalRendering from "./ConditionalRendering.vue";
// import Methods from './Methods.vue';
import EventHandling from './EventHandling.vue';

export default {
  name: "App",
  data(){ 
    return {
      greet: "Hello",
      name: "Batman",
      channel: "<b>Codevolution</b>",
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a Prize!</a>`,
      headingId: "heading",
      isDisabled: false, 
      status: "success",
      isPromoted: true,
      isSoldOut: true,
      highlightColor: "orange",
      headerSize: 50,
      headerStyleObject: {
        color: "orange",
        fontSize: "50px",
        padding: "20px"
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px"
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
        padding: "20px"
      },
      dangerStyleObject: {
        color: "darkred",
        backgoundColor: "red",
        border: "1px solid darkred"
      }
    };
  },
  components: {
    EventHandling
  }
}

</script>

<template>
  <div>
    <!-- <div>{{ greet }} {{ name }}</div>
    <div v-text="channel"></div> -->
    <!-- <div v-text="name">Hello</div> -->

    <!-- <div v-html="channel"></div>
    <div v-html="hack"></div> -->
    <!-- <div>{{ hack }}</div> -->

    <!-- <h2 :id="headingId">Heading</h2>
    <button :disabled="isDisabled">Bind</button>

    <h2 class="underline">Underlined Text</h2>

    <h2 class="underline" :class="status">Status</h2>

    <h2 :class="{'promoted' : isPromoted}">Promoted Movie</h2>

    <h2 :class="isSoldOut ? 'sold-out' : 'new'">Soldout? Movie</h2>

    <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>

    <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">Array Conditional Movie</h2>

    <h2 :class="{
      'promoted': isPromoted,
      'new': !isSoldOut,
      'sold-out': isSoldOut
    }">Object Conditional Movie</h2> -->

    <!-- <h2 :style="{color: highlightColor, 'font-size': headerSize + 'px'}">Inline Styles</h2> -->
    <!-- <h2 :style="{color: highlightColor, fontSize: headerSize + 'px', padding: '20px'}">Inline Styles</h2>

    <h2 :style="headerStyleObject">Style Object</h2>

    <div :style="[baseStyleObject, successStyleObject]">Success Styles</div>

  <div :style="[baseStyleObject, dangerStyleObject]">Danger Styles</div> -->

   <!-- <ConditionalRendering /> -->
   <!-- <Methods /> -->
    <EventHandling />

  </div>
</template>

<style scoped>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>
