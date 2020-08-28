<template>
    <div class="worldwide-page">
        <mainMenu/>
        <div class="bg-color">
            <div class="cta">
                <a href="/" class="btn btn-back">Back to My Wall</a>
            </div>
            <div class="worldwide-icon">
                <div class="icon-holder">
                    <img src="~assets/default-img/globe.svg"/>
                </div>
            </div>
        </div>
        <div class="post-container">
            <h2 class="title">Worldwide</h2>
            <publicPostContent/>
            <publicPostContent/>
            <publicPostContent/>
            <publicPostContent/>
        </div>
    </div>
</template>

<script>
import publicPostContent from '~/components/Post/publicPostContent';
import mainMenu from '~/components/Nav/menu';
export default {
    name: "worldwide",
    components: {
        publicPostContent,
        mainMenu
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

a,button {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
</style>

<style scoped>
.cta , .post-container {
    max-width:800px;
    margin:0 auto;
}
.worldwide-icon {
    padding:0px 20px;
}
.icon-holder {
    width:100px;
}
.cta {
    padding:20px;
    text-align:right;
}
.bg-color {
    background: rgb(0,201,255);
    background: linear-gradient(156deg, rgba(0,201,255,1) 0%, rgba(146,254,157,1) 100%);
    padding-bottom:150px;
    height:318px;
}
.post-container {
    padding:10px 20px;
    margin-top:-150px;
}
.title {
  padding-top:30px;
  color:#fff;
  padding-bottom:20px;
  letter-spacing: 0.4px;
  font-size:2rem;
}
.btn {
    border:2px solid;
    padding:10px 20px;
    font-size:14px;
    border-radius:100px;
    letter-spacing: 0.45px;
    cursor:pointer;
}
.btn-back {
    border:none;
    color:#fff;
    font-weight:bold;
    background:#fff;
    font-family:'Roboto', sans-serif;
    letter-spacing:0.4px;
    outline:none;
    text-decoration: none;
    margin-left:10px;
    color:#0F4C75;
}
</style>