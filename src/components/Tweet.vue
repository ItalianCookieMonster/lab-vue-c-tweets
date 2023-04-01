<template>
  <div class="tweet">
    <Profile-image :image="tweet.user.image"/>

    <div class="body">
      <div class="top">
        <User :userData="tweet.user"/>
        <timestamp :time="tweet.timestamp"/>
      </div>

      <Message :message="tweet.message"/>

      <Actions />
      
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>

<script>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Meesage.vue';
import Actions from './Actions.vue'
export default {
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions
  },
  props: ['tweet']
}

</script>
