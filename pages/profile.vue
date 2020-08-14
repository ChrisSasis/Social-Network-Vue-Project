<template>
    <div class="profile-page">
        <mainHeader/>
        <mainMenu/>
        <profileContent/>
        <postContent/>
        <postContent/>
        <postContent/>
        <postContent/>
        <postContent/>
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
</style>