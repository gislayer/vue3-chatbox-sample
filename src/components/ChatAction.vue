<template>
  <div class="card-footer p-3">
    <div class="form-outline">
      <textarea placeholder="Write Your Message Here!..." @keydown.enter="addText" v-model="text" class="form-control" id="textAreaExample"
        rows="3"></textarea>
    </div>
  </div>
</template>

<script>
  export default {
    name: "ChatAction",
    data() {
      return {
        text: '',
      }
    },
    inject: ['addMessage', 'users', 'sender'],
    methods: {
      addText() {
        if (this.text == '') {
          return false;
        }
        this.addMessage(this.sender, this.text);
        this.text = '';
      }
    }
  }
</script>