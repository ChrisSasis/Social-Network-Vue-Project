<template>
    <div class="create-page">
        <div class="postarea-container">
            <div class="post-content">
                <div class="post-area">
                    <!-- <textarea name="" id="" cols="30" rows="10"
                    placeholder="Share Something..." class="post-textarea"></textarea> -->
                    <p contenteditable="true" class="post-textarea"></p>
                </div>
            </div>
            <div class="post-footer">
                <!-- <button class="btn-main btn-icon">
                    <input type="file">
                    <img  src="~assets/default-img/add.svg" alt="">
                </button> -->
                <div class="post-public">
                    <input type="checkbox" id="public" value="public">
                    <div class="public-bg"></div>
                    <label for="public">Worldwide</label>
                </div>
                
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
button {
    outline:none;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
.create-page {
    padding:20px;
    max-width:800px;
    margin:0 auto;
}
.post-user-img {
    width:30px;
    height:30px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    border-radius:100px;
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
    min-height:200px;
    position:relative;
}
.post-textarea:before {
    content:'Share Something...';
    color:#222;
}
.post-textarea:focus:before {
    content:'';
}
.post-footer {
    padding:10px 0px;
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
    width:34px;
    height:34px;
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
    font-size:14px;
    font-weight: 600;
}
.post-public {
    position:relative;
    max-width:150px;
    padding:7px 20px;
    text-align:center;
    /* background:#ececec; */
    border-radius: 100px;
    cursor: pointer;
    overflow:hidden;
}
.post-public input {
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    opacity: 0;
    cursor: pointer;
    z-index: 10;
    background:transparent
}
.public-bg {
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    z-index:-1;
    background:#ececec;
}
.post-public input:checked ~ .public-bg {
    background:#206a5d;
}
.post-public input:checked ~ label {
   color:#fff;
}
</style>