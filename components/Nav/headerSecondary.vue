<template>
    <div class="header">
        <a href="#" class="header-back">
            <div class="header-back-holder">
                <img src="~assets/default-img/ion_arrow-back.svg" alt="">
            </div>
        </a>
    </div>
</template>

<script>
export default {
    name: "headerSecondary"
}
</script>

<style scoped>
img {
    width:100%;
}
.header {
    padding:10px;
    box-shadow:0px 0px 4px rgba(0,0,0,0.1);
}
.header-back {
    width:30px;
    height:30px;
    border-radius:100px;
    display:block;
    background:#0F4C75;
    position:relative;
}
.header-back-holder {
    width:22px;
    position:absolute;
    top:55%;
    left:0;
    right:0;
    margin:0 auto;
    transform:translateY(-55%);
}
</style>