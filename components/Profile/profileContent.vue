<template>
    <div>
        <div class="profile-content">
            <div class="profile-holder">
                <div class="profile-image-holder">
                    <div class="profile-image"  style="background-image:url('https://pbs.twimg.com/profile_images/1210618202457292802/lt9KD2lt_400x400.jpg')"></div>
                </div>
                <div class="profile-cta">
                    <button class="btn btn-follow">
                        Settings
                    </button>
                    <!-- <button class="btn btn-edit">
                        Edit Profile
                    </button> -->
                </div>
            </div>
            <div class="profile-details">
                <h2 class="user-name">John Appleased</h2>
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
.profile-content {
    max-width:800px;
    margin:0 auto;
}
.profile-image {
    width:100px;
    height:100px;
    border-radius:100px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    margin:0 auto;
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
    width:100%;
}
.btn {
    border:2px solid;
    padding:10px 20px;
    font-size:14px;
    border-radius:100px;
    letter-spacing: 0.45px;
    cursor:pointer;
}
.btn-follow {
    border:none;
    color:#fff;
    font-weight:bold;
    background:rgba(0,0,0,0.4);
    font-family:'Roboto', sans-serif;
    letter-spacing:0.4px;
    outline:none;
}
.btn-edit {
    border-color:#0F4C75;
    color:#0F4C75;
    font-weight:bold;
    background:transparent;
}
.btn-follow:hover, 
.btn-follow:active {
    background: rgba(0,0,0,0.4);
    color:#fff;
}
.profile-details {
    padding:0px 20px;
}
.user-name {
    color:#fff;
    font-weight: 300;
}


</style>