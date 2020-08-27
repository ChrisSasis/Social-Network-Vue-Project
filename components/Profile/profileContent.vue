<template>
    <div>
        <div class="profile-content">
            <div class="profile-holder">
                <div class="profile-image-holder">
                    <div class="profile-image"  style="background-image:url('https://pbs.twimg.com/profile_images/1210618202457292802/lt9KD2lt_400x400.jpg')"></div>
                </div>
                <div class="profile-cta">
                    <button class="btn btn-follow" @click="showMenu">
                        Settings
                    </button>
                </div>
            </div>
            <div class="profile-details">
                <h2 class="user-name">
                    <!-- {{ name }} -->
                    John Appleased
                </h2>
            </div>
        </div>
        <!-- settings popup -->
        <div  v-bind:class="{show: settingsModal}" class="settings-modal modal hide">
            <div class="modal-holder" @click="hideMenu"></div>
            <div class="modal-container">
                <div class="modal-header">
                    <h3>Settings</h3>
                </div>
                <div class="modal-content">
                    <ul class="settings-list">
                        <li>
                            <a href="/edit-profile" class="settings-link">Edit Profile</a>
                        </li>
                        <li>
                            <a href="/change-password" class="settings-link">Change Password</a>
                        </li>
                        <li>
                            <a href="/theme" class="settings-link">Theme</a>
                        </li>
                        <li>
                            <a href="/login" class="settings-link">Log Out</a>
                        </li>
                    </ul>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "profileContent",
    props: ['name'],
    data() {
        return {
            settingsModal: false
        }
    },
    methods:{
        showMenu() {
            this.settingsModal = true;
        },
        hideMenu() {
            this.settingsModal = false;
        }
    },
    head () {
      return {
        bodyAttrs: {
          class: this.settingsModal ? 'overflow-hidden' : ''
        }
      }
    },
}
</script>

<style>
.overflow-hidden {
    overflow: hidden;
}
button {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
</style>

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
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
}
.btn-follow {
    border:none;
    color:#fff;
    font-weight:bold;
    background:rgba(0,0,0,0.4);
    font-family:'Roboto', sans-serif;
    letter-spacing:0.4px;
    outline:none;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
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
.show {
    display:block !important;
}
.hide {
    display:none;
}
/* modal */
.modal {
    display: none;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    z-index: 100;
}
.modal-holder {
    background:rgba(0,0,0,0.8);
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    cursor:pointer;
}
.modal-container {
    position:absolute;
    bottom:0;
    left:0;
    right:0;
    width:100%;
    background:#fff;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    max-width:800px;
    margin:0 auto;
}
.modal-header {
    padding:15px 20px;
    font-family: 'Roboto', sans-serif;
    font-size:1.3rem;
}
.settings-link {
    display:block;
    padding:15px 20px;
    border-top:1px solid #ececec;
    text-decoration: none;
    color:#000;
    font-size: 16px;
}
.settings-list {
    list-style-type: none;
    margin:0;
    padding:0;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
@media screen and (min-width:700px) {
    .modal-container {
        top:50%;
        transform:translateY(-50%);
        bottom:inherit;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
    }
}
</style>