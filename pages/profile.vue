<template>
    <div class="profile-page">
        <!-- <mainHeader/> -->
        <mainMenu/>
        <div class="bg-color">
          <profileContent/>
        </div>
        <div class="post-container">
          <h2 class="my-wall-title">My Wall</h2>
          <postContent/>
          <postContent/>
          <postContent/>
          <postContent/>
          <postContent/>
        </div>
    </div>
</template>

<script>

import mainHeader from '~/components/Nav/header';
import mainMenu from '~/components/Nav/menu';
import postContent from '~/components/Post/postContent';
import profileContent from '~/components/Profile/profileContent';

export default {
    name: "profilePage",
    components: {
        mainHeader,
        mainMenu,
        postContent,
        profileContent
    }
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