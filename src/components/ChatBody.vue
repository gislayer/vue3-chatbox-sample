<template>
  <div class="card-body chatScroll">
    <ChatMessage 
      :key="index"
      :message="message"
      v-for="(message,index) in chatData.messages"
    />
  </div>
</template>

<script>
  import ChatMessage from '@/components/ChatMessage';
  export default {
    name: "ChatBody",
    components:{
      ChatMessage
    },
    inject:['chatData'],
    computed:{

    }
  }
</script>