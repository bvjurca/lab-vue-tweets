<template>
  <div class="tweet">
    <ProfileImage :image="user.image" />
    <div class="body">
      <div class="top">
        <User :user="user" />

        <Timestamp :timestamp="timestamp" />
      </div>

      <Message :message="message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

export default {
  props: {
    user: {
      name: String,
      handle: String,
      image: String,
    },
    timestamp: String,
    message: String,
  },
  components: { ProfileImage, User, Timestamp, Message, Actions },
};
</script>


<style scoped>
a {
  color: #42b983;
}
</style>
