<template>
    <div v-if="sender==message.user_id" class="d-flex flex-row justify-content-end mb-4">
      <div class="p-3 me-2 borderRight">
        <p class="small mb-0">{{ message.text }}</p>
      </div>
      <img :src="getImage" alt="avatar 1"
        style="width: 45px; height: 100%;">
    </div>
    <div v-else class="d-flex flex-row justify-content-start mb-4">
      <img :src="getImage" alt="avatar 1"
        style="width: 45px; height: 100%;">
      <div class="p-3 ms-2 borderLeft">
        <p class="small mb-0">{{ message.text }}</p>
      </div>
      
    </div>
</template>

<script>
  export default {
    props:{
      message:{
        type: Object,
        require: true
      }
    },
    inject:['users','sender'],
    computed:{
      getImage(){
        var user = this.users.find((u) => u.id===this.message.user_id);
        return user.img;
      }
    }
  }
</script>