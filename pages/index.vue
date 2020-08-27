<template>
    <div class="profile-page">
        <!-- <mainHeader/> -->
        <!-- <mainMenu :color="this.user.theme"/> -->
        <mainMenu/>
        <!-- <div class="bg-color" :style="'background-color:'+this.user.theme"> -->
        <div class="bg-color">
          {{color}}
          <!-- <profileContent :name="this.user.name"/> -->
          <profileContent/>
        </div>
        <div class="post-container">
          <h2 class="my-wall-title">My Wall</h2>  
          <!-- <div v-for="post in posts" :key="post.id"> -->
            <!-- <postContent :post="post.content" :created="post.created_at"/> -->
            <postContent/>
            <postContent/>
            <postContent/>
            <postContent/>
            <postContent/>
            
          <!-- </div> -->
        </div>
    </div>
</template>

<script>

import mainHeader from '~/components/Nav/header';
import mainMenu from '~/components/Nav/menu';
import postContent from '~/components/Post/postContent';
import profileContent from '~/components/Profile/profileContent';
import userQuery from "~/apollo/queries/user";
import postQuery from "~/apollo/queries/posts";
import gql from 'graphql-tag';

export default {
    name: "index",
    components: {
        mainHeader,
        mainMenu,
        postContent,
        profileContent
    },
    data: () => {
      return {
        user: [],
        posts: [],
        post: '',
        post_created: '',
      }
    },
    async fetch() {
      try {
        const response = await this.$apollo.query({
          query: gql `${userQuery}`
        });
        this.user = response.data.user;
      } catch (error) {
        console.log(error);
      }

      try {
        const response = await this.$apollo.query({
          query: gql `${postQuery}`,
          variable: {id: 1}
        });
        this.posts = response.data.post_by_user;
      } catch (error) {
        console.log(error);
      }
    },
}
</script>


<style>
* {
  box-sizing: border-box;
  padding:0;
  margin:0;
  font-family:'Roboto', sans-serif;
}

img {
  width:100%;
}

</style>


<style scoped>
.post-container {
    max-width:800px;
    margin:0 auto;
}
.profile-page {
  padding-bottom:100px;
}
.my-wall-title {
  padding-top:30px;
  padding-left:20px;
  color:#fff;
}
.bg-color {
  background-color:#0F4C75;
  padding-bottom:150px;
}
.post-container {
  margin-top:-150px;
}
</style>