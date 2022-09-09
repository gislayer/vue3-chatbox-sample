<template>
  <div class="container py-5">
    <div class="row d-flex justify-content-center">
      <div class="col-md-8 col-lg-6 col-xl-4">
        <div class="card" id="chat1" style="border-radius: 15px;">
          <ChatBox/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChatBox from './components/ChatBox.vue'

export default {
  name: 'App',
  components: {
    ChatBox
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
