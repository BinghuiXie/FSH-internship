<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <PostHeader title="博客标题A" postTime="2019.11.20" author="不会拉小提琴的左脚" />
    <SlotTest>
      <template v-slot:slot-test-header>
        <p>I'm slot test header, technically, I'm useless ,only for the demo</p>
      </template>
      <template v-slot:slot-test-main>
        <p>I want to be the main part of a post, however, the author set me as the main part of the slot name demo!</p>
      </template>
      <template v-slot:slot-test-footer>
        <p>I'm the footer of this demo, BTW, the author's english is shit!</p>
      </template>
      <template>
        {{ slotProps.user.lastName }}
      </template>
    </SlotTest>
  </div>
</template>

<script>
import PostHeader from "./components/PostHeader";
import SlotTest from "./components/SlotTest.vue"

export default {
  name: 'app',
  components: {
    SlotTest,
    PostHeader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
