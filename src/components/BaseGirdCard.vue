<template>
     <div class="ui card" style="margin-top:0;">
      <div class="image">
        <img style="max-height: 240px;" :src="user.avatar_url">
      </div>
      <div class="content">
        <a :href= "user.url" class="header">{{ user.name }}</a>
        <div class="meta">
          <span class="date">Joined in {{ user.created_at }}</span>
        </div>
        <div class="description">
          {{ user.bio }}
        </div>
      </div>
      <div class="extra content">
        <a>
          <i class="user icon"></i>
          {{ user.followers }} Friends
        </a>
      </div>
    </div>
</template>
<script>
import axios from 'axios'
export default{
    props:{
        username: {
            type:String,
            required: true,
        }
    },
    data() {
        return {
            user: {},
        }
    },
    mounted()
    {
    
    },
   async created()
    {
        const response = await axios
      .get(`https://api.github.com/users/${this.username}`);
        this.user = response.data;
    }    
}
</script>