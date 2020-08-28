<template>
    <div class="menu-fixed">
        <div class="menu">
            <!-- <a href="/create" class="menu-btn" :style="'background-color:'+ color"> -->
            <a href="/create" class="menu-btn">
                <div class="menu-btn-icon">
                    <img src="~assets/default-img/Vector-1.svg"/>
                </div>
            </a>
            <a href="/worldwide" class="menu-btn-worldwide" v-bind:class="{ 'hide': iconShow }">
                <div class="menu-btn-icon">
                    <img src="~assets/default-img/globe.svg"/>
                </div>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "mainMenu",
    props: ['color'],
    data() {
        return {
            iconShow: false,
        }
    },
    created() {
        if(this.$route.fullPath == "/worldwide") {
            this.iconShow = true;
        }
    }
}
</script>

<style scoped>
.hide {
    display:none !important;
}
img {
    width:100%;
}
.menu-fixed {
    position:fixed;
    bottom:20px;
    left:0;
    right:0;
    margin:0 auto;
    max-width:800px;
    width:100%;
    z-index:100;
}
.menu {
    height:50px;
    position:relative;
}
.menu-btn {
    display:block;
    background-color: #0F4C75;
    width:60px;
    height:60px;
    box-shadow:0px 4px 4px rgba(0,0,0,0.3);
    border-radius:100px;
    text-align:center;
    padding:13px 0px;
    position:absolute;
    top:0;
    right:20px;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
.menu-btn-icon {
    width:30px;
    margin:0 auto;
}
.menu-btn-worldwide .menu-btn-icon {
    width:35px;
    margin:0 auto;
}

.menu-btn-worldwide {
    display:block;
    background: rgb(0,201,255);
    background: linear-gradient(156deg, rgba(0,201,255,1) 0%, rgba(146,254,157,1) 100%);
    width:60px;
    height:60px;
    box-shadow:0px 1px 4px rgba(0,0,0,0.3);
    border-radius:100px;
    text-align:center;
    padding:13px 0px;
    position:absolute;
    top:0;
    left:20px;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
</style>