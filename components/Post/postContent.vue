<template>
    <div>
        <div class="post-holder">
            <div class="post-wrapper">
                <div class="post-user">
                    <div class="post-user-img" style="background-image:url('https://pbs.twimg.com/profile_images/1210618202457292802/lt9KD2lt_400x400.jpg')"></div>
                </div>
                <div class="post-content">
                    <div class="post-header">
                        <span class="post-creator">John Appleased</span>
                        <span class="post-date">12 hrs ago</span>
                    </div>
                    <div class="post-body">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni aut odit, soluta esse velit modi? Laboriosam odit repellat enim ea aperiam excepturi? Animi molestiae nostrum natus commodi quod officia labore?
                    </div>
                    <div class="post-footer">
                        <button class="btn">
                            <div class="btn-icon">
                                <img src="~assets/default-img/heart-active.svg">
                            </div>
                            <span class="btn-count">12k</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "postContent",
}
</script>

<style scoped>
.post-holder {
    padding:10px 20px;
}
.post-wrapper {
    display:flex;
    width:100%;
}
.post-user-img {
    width:30px;
    height: 30px;
    border-radius:100px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}
.post-content {
    margin-left:10px;
    background-color:#F9F9F9;
    padding:10px 15px;
    border-radius:10px;
}
.post-creator ,
.post-date{
    display:block;
    width:100%;
}
.post-creator {
    font-weight:700;
    font-size:14px;
}
.post-date {
    font-size:12px;
    padding-top:2px;
    color:#BABABA;
}
.post-body {
    padding:10px 0px;
    font-size:14px;
    letter-spacing: 0.4px;
}
.btn {
    display:flex;
    align-items: center;
    padding:8px 15px;
    background:#e0e0e0;
    border:none;
    border-radius:100px;
}
.btn-icon {
    width:18px; 
    height:16px;
}
.btn-count {
    padding-left:5px;
    font-size:14px;
    font-weight:bold;
}
</style>