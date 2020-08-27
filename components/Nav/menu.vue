<template>
    <div class="menu-fixed">
        <div class="menu">
            <a href="/create" class="menu-btn" :style="'background-color:'+ color">
                <div class="menu-btn-icon">
                    <img src="~assets/default-img/Vector-1.svg"/>
                </div>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "mainMenu",
    props: ['color']
}
</script>

<style scoped>
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
</style>