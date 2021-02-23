<template>
  <div class="test">
    <h1>Hola {{ name }}</h1>
    <a v-bind:href="linkUrl"> link</a>
    <a v-bind:[attrKey]="attrKey"> link</a>
    <div class="message" v-if="msgVisibility">Message</div>
    <div class="message" v-else>AnotherMessage</div>
    <div v-show="msgVisibility">BLOCK</div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data: () => ({
    name: "Test",
    linkUrl: "https://google.com",
    attrKey: "href",
    msgVisibility: false,
  }),
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
