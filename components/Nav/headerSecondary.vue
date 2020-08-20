<template>
    <div class="header">
        <a href="/" class="header-back">
            Back To My Wall
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
    text-align:right;
    padding:10px 20px;
    max-width:800px;
    margin:0 auto;
}
.header-back {
    border-radius:100px;
    display:inline-block;
    background:#0F4C75;
    position:relative;
    padding:10px 20px;
    color:#fff;
    font-family: 'Roboto', sans-serif;
    text-align:center;
    text-decoration:none;
    max-width:180px;
    font-size:14px;
    font-weight: bold;
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