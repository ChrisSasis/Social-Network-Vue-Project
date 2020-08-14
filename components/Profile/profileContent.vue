<template>
    <div>
        <div class="profile-cover" style="background-image:url('https://images.unsplash.com/photo-1597341509852-a7ec52333ff0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1534&q=80')"></div>
        <div class="profile-content">
            <div class="profile-holder">
                <div class="profile-image-holder">
                    <div class="profile-image"  style="background-image:url('https://pbs.twimg.com/profile_images/1210618202457292802/lt9KD2lt_400x400.jpg')"></div>
                </div>
                <div class="profile-cta">
                    <button class="btn btn-follow">
                        Follow
                    </button>
                    <!-- <button class="btn btn-edit">
                        Edit Profile
                    </button> -->
                </div>
            </div>
            <div class="profile-details">
                <h2 class="user-name">John Appleased</h2>
                <p class="user-about">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sunt provident vitae minima nobis molestiae excepturi doloribus eligendi unde beatae nesciunt distinctio, similique aperiam aut vel porro architecto repellat ullam facere!</p>
                <div class="profile-following-post"> 
                    12 Post | <a href="#" class="following-link">3 Following</a> 
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "profileContent"
}
</script>

<style scoped>
.profile-cover {
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height:100px;
}
.profile-image {
    width:100px;
    height:100px;
    border-radius:100px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}
.profile-holder {
    display: inline-flex;
    flex-wrap:nowrap;
    width:100%;
    padding:20px;
}
.profile-cta {
    padding-left:10px;
    text-align: right;
    width:80%;
}
.btn {
    border:2px solid;
    padding:10px 20px;
    font-size:14px;
    border-radius:100px;
    letter-spacing: 0.45px;
}
.btn-follow {
    border-color:#0F4C75;
    color:#fff;
    font-weight:bold;
    background:#0F4C75;
    
}
.btn-edit {
    border-color:#0F4C75;
    color:#0F4C75;
    font-weight:bold;
    background:transparent;
}
.btn-follow:hover, 
.btn-follow:active {
    background: #0F4C75;
    color:#fff;
}
.profile-details {
    padding:0px 20px;
}
.user-name {
    color:#0F4C75;
}
.user-about {
    letter-spacing: 0.45px;
    font-size:14px;
    padding:10px 0px;
    line-height: 19px;
}
.profile-following-post {
    padding:0px 0px 20px;
}
.following-link {
    color:#0F4C75;
    font-weight:bold;
    text-decoration: none;
    display:inline-block;
    padding:10px;
}

</style>