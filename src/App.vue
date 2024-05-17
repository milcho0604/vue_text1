<template>
  <div id="app">
    <h1>MyText1</h1>
    <MyText1 title="TEXT1" description="첫째 컴포넌트" color="#ffb"  v-on:send="showValue" />
    <MyText1 title="TEXT2" color="#afa"  v-on:send="showValue" />
  </div>
</template>

<script>
import MyText1 from './MyText1.vue';

export default {
  name: "App",
  methods: {
    showValue(value) {
      alert(value);
    }
  },
  components: { MyText1 }
}
</script>

<style scoped>
div#app { padding: 0 30px 30px 30px; margin: 30px auto; max-width: 400px;
      border: 1px solid #ccc; box-shadow: 3px 3px 3px #aaa; }
</style>
