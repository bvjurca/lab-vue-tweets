<template>
  <div class="tweet">
    <ProfileImage :image= "image" />

    <div class="body">
      <div class="top">
        <span class="user">
          <User :user= "user" />
        </span>

        <Timestamp :timestamp= "timestamp" />
      </div>

      <Message :message="message" />

      <div class="actions">
        <!-- Font Awesome icons -->
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
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';

export default{
  props: {
    user: {
      name: String,
      handle: String,
      image: String,
    },
    timestamp: String,
    message: String,
  },
  components: { ProfileImage, User, Timestamp, Message }
}
 
</script>


<style scoped>
a {
  color: #42b983;
}
</style>
