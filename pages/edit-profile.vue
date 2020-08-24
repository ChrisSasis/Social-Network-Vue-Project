<template>
    <div class="edit-profile-page">
        <div class="bg-color">
            <div class="cta">
                <a href="/" class="btn btn-back">
                    Back to My Wall
                </a>
                <button class="btn btn-follow" @click="showMenu">
                    Settings
                </button>
            </div>
        </div>
        <div class="form-container">
            <h2 class="title">Edit Profile</h2>
            <editProfile/>
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
                            <a href="#" class="settings-link">Theme</a>
                        </li>
                        <li>
                            <a href="#" class="settings-link">Log Out</a>
                        </li>
                    </ul>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
import mainHeader from '~/components/Nav/header';
import mainMenu from '~/components/Nav/menu';
import editProfile from '~/components/Forms/editProfile';

export default {
    // name: "editrofile",
    components: {
        mainHeader,
        mainMenu,
        editProfile
    },
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
* {
  box-sizing: border-box;
  padding:0;
  margin:0;
  font-family:'Roboto', sans-serif;
}

img {
  width:100%;
}

</style>

<style scoped>
.cta, .form-container {
    max-width:800px;
    margin:0 auto;
}
.cta {
    padding:20px;
    text-align: right;
}
.title {
  padding-top:30px;
  color:#fff;
  padding-bottom:20px;
}
.bg-color {
    background-color:#0F4C75;
    padding-bottom:150px;
    height:318px;
}
.form-container {
    padding:10px 20px;
    margin-top:-150px;
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
    text-decoration: none;
    margin-left:10px;
}
.btn-back {
    border:none;
    color:#fff;
    font-weight:bold;
    background:#fff;
    font-family:'Roboto', sans-serif;
    letter-spacing:0.4px;
    outline:none;
    text-decoration: none;
    margin-left:10px;
    color:#0F4C75;
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