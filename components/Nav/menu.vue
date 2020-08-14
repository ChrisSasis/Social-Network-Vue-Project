<template>
    <div class="menu-fixed">
        <div class="menu">
            <div class="menu-item">
                <a href="#" class="menu-link">
                    <div class="menu-icon-holder">
                        <img src="~assets/default-img/Vector-3.svg"/>
                    </div>
                </a>
            </div>
            <div class="menu-item">
                <a href="#" class="menu-link">
                    <div class="menu-icon-holder">
                        <img src="~assets/default-img/Vector-2.svg"/>
                    </div>
                </a>
            </div>
            <div class="menu-item">
                <a href="#" class="menu-link">
                    <div class="menu-icon-holder">
                        <img src="~assets/default-img/Vector-1.svg"/>
                    </div>
                </a>
            </div>
            <div class="menu-item">
                <a href="#" class="menu-link">
                    <div class="menu-icon-holder">
                        <img src="~assets/default-img/Vector.svg"/>
                    </div>
                </a>
            </div>
            <div class="menu-item">
                <a href="/profile" class="menu-link">
                    <div class="user-icon-holder" style="background-image:url('https://pbs.twimg.com/profile_images/1210618202457292802/lt9KD2lt_400x400.jpg')">
                        <img src="" alt="">
                    </div>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "mainMenu",
}
</script>

<style scoped>
.menu-fixed {
    width:100%;
    position:fixed;
    bottom:0;
    left:0;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    overflow: hidden;
}
.menu {
    display:grid;
    grid-template-columns: 20% 20% 20% 20% 20%;
    background:#0F4C75;
}
.menu-link {
    display:block;
    padding:15px 10px;
}
.menu-icon-holder {
    width:20px;
    height:25px;
    margin:0 auto;
}
.user-icon-holder {
    width:25px;
    height:25px;
    border-radius:100px;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    margin:0 auto;
}
</style>