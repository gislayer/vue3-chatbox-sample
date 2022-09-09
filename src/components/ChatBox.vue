<template>
  <ChatHeader/>
  <ChatBody/>
  <ChatAction/>
</template>

<script>
import ChatHeader from '@/components/ChatHeader';
import ChatBody from '@/components/ChatBody';
import ChatAction from '@/components/ChatAction';
export default {
  name: 'ChatBox',
  components:{
    ChatHeader,
    ChatBody,
    ChatAction,
  },
  data(){
    return {
      title:`Let's Chat!...`,
      chatData:{
        sender:1,
        users:[
          {
            id:1,
            img:'https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-chat/ava1-bg.webp',
            name:'Ali Kılıç'
          },
          {
            id:2,
            img:'https://mdbcdn.b-cdn.net/img/Photos/new-templates/bootstrap-chat/ava2-bg.webp',
            name:'J. W.'
          },
          ],
        messages:[]
      },
      demoMessages:[
        {
          user_id:2,
          text:'Auto Test Message 1'
        },
        {
          user_id:2,
          text:'Auto Test Message 2'
        },
        {
          user_id:2,
          text:'Auto Test Message 3'
        }
      ]
    };
  },
  methods:{
    addMessage(user_id,text){
      this.chatData.messages.push({
        user_id,
        text
      });
      // This is for auto message. you can delete it when you use websocket
      setTimeout(() =>{
        this.chatData.messages.push(this.demoMessages[Date.now()%3]);
      },2000)
    }
  },
  provide(){
    return {
      title:this.title,
      users:this.chatData.users,
      chatData:this.chatData,
      addMessage:this.addMessage,
      sender:this.chatData.sender,
    }
  }
}
</script>
