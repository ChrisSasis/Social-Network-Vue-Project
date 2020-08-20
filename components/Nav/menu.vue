<template>
    <div class="menu-fixed">
        <div class="menu">
            <a href="/create" class="menu-btn">
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
}
</script>

<style scoped>
img {
    width:100%;
}
.menu-fixed {
    position:fixed;
    bottom:15px;
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
    width:50px;
    height:50px;
    box-shadow:0px 4px 4px rgba(0,0,0,0.3);
    border-radius:100px;
    text-align:center;
    padding:10px 0px;
    position:absolute;
    top:0;
    right:20px;
}
.menu-btn-icon {
    width:25px;
    margin:0 auto;
}
</style>