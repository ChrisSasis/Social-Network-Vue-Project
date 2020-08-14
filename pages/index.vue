<template>
  <div class="home-page">
    <mainHeader/>
    <mainMenu/>
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

export default {
  components: {
    mainHeader,
    mainMenu,
    postContent
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
.home-page {
  padding-bottom:100px;
}
</style>