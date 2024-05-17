<template>
  <div :style="{ backgroundColor: color }">
    <h2>{{ title }} - <small>{{ description }}</small></h2>
    <input type="text" v-model="message" />
    <button type="button" @click="$emit('send', message)"> 전달 </button> 
  </div>
</template>

<script>
export default {
  name: "MyText1",
  props: {
    title: { type: String, required: true},
    description: { type: String, default: "작업"},
    color: { type: String, default: "#fff"}
  },
  data() {
    return { text: "입력하세요."};
  }
}
</script>

<style scoped>
  div { border: 1px solid gray; padding: 0 20px 20px 20px; margin-top: 10px; }
  input { padding: 5px; margin-right: 5px; }
  button { padding: 0.4em 1em; margin-right: 5px; }
</style>
