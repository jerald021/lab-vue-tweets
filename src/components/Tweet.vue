<template>
  <div className="tweet">
    <ProfileImage :user="tweet.user"/> 
    <div className="body">
      <div className="top">
        <User :user="tweet.user"/>       
        <Timestamp :timestamp="tweet.timestamp"/>       
      </div>

      <Message :message="tweet.message"/>      
      <Actions/>
    </div>     

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Actions from "./Actions.vue";
import Message from "./Message.vue";
import Timestamp from "./Timestamp.vue";

export default {
  components: {
    ProfileImage,
    User,
    Actions,
    Message,
    Timestamp,
},
  props:{
    tweet:{
      type: Object,
      user:{
        type: Object,
      },
    }    
  }  
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>