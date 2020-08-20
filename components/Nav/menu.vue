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
    right:15px;
    z-index:100;
}
/* .menu-fixed {
    width:100%;
    position:fixed;
    bottom:0;
    left:0;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    overflow: hidden;
} */
.menu-btn {
    display:block;
    background-color: #0F4C75;
    width:50px;
    height:50px;
    box-shadow:0px 4px 4px rgba(0,0,0,0.3);
    border-radius:100px;
    text-align:center;
    padding:10px 0px;
}
.menu-btn-icon {
    width:25px;
    margin:0 auto;
}
</style>