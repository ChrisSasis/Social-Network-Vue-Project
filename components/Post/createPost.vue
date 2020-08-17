<template>
    <div class="create-page">
        <div class="postarea-container">
            <div class="post-content">
                <div class="post-user-img" style="background-image:url('https://pbs.twimg.com/profile_images/1210618202457292802/lt9KD2lt_400x400.jpg')"></div>
                <div class="post-area">
                    <textarea name="" id="" cols="30" rows="10"
                    placeholder="Share Something..." class="post-textarea"></textarea>
                </div>
            </div>
            <div class="post-footer">
                <button class="btn-main btn-icon">
                    <input type="file">
                    <img  src="~assets/default-img/add.svg" alt="">
                </button>
                <button class="btn-main btn-post">
                    Post
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "createPost"
}
</script>

<style scoped>
.create-page {
    padding:20px 10px;
}
.post-content {
    display:flex;
    flex-wrap:nowrap;
    width:100%;
}
.post-user-img {
    width:30px;
    height:30px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    border-radius:100px;
}
.post-area {
    padding-left:20px;
    width:90%;
}
.post-textarea {
    font-family:'Open Sans', sans-serif;
    letter-spacing: 0.4px;
    background: #F9F9F9;
    border:none;
    border-radius:10px;
    resize:none;
    padding:15px;
    width:100%;
    display: block;
    outline:none;
    font-size:14px;
}
.post-footer {
    padding:10px;
    position:relative;
}
.btn-main {
    border:none;
    border-radius:100px;
    background: #0F4C75;
    display:inline-block;
    vertical-align: top;
}
.btn-icon {
    width:30px;
    height:30px;
    padding-top:5px;
    overflow:hidden;
    position:relative;
    outline:none;
}
.btn-icon input {
    opacity: 0;
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
}
.btn-icon img {
    width:100%;
}
.btn-post {
    padding:7px 20px;
    color:#Ffff;
    letter-spacing:0.4px;
    position:absolute;
    top:10px;
    right:0;
}
</style>