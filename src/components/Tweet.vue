<template>
  <div className="tweet">
    <!-- <span className="name">{{tweet.user.name}}</span> -->    
    <img
      :src="tweet.user.image"
      className="profile"
      alt="profile"
    />

    <div className="body">
      <div className="top">
        <span className="user">
          <span className="name">{{tweet.user.name}}</span>
          <span className="handle">{{tweet.user.handle}}</span>
        </span>
        
        <span className="timestamp">{{tweet.timestamp}}</span>
      </div>

      <p className="message">
        {{tweet.message}}
      </p>

      <div className="actions">
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>     

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
export default {
  props:{
    tweet:{
      user:{
        name:{
          type: String,
        },
        image:{
          type: String,
        },
        handle:{
          type: String,
        },      
      },
      timestamp:{
        type: String,
      },
      message:{
        type: String,
        default:'this is the message',
      },
    },    
  }    
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>