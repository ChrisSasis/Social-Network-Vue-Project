<template>
    <div class="edit-profile-page">
        <div class="bg-color" :style="'background-color:'+this.newColor+''">
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
            <h2 class="title">Theme</h2>
            <div class="theme-picker">
                <ul class="theme-list">
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#BA7967')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" checked @change="changeTheme('#0F4C75')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#5E6F64')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#EEBB4D')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#BB3B0E')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#F08A5D')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#6EBFB5')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#FCCBCB')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#B134C6')">
                        <span class="check"></span>
                    </li>
                    <li class="theme-item">
                        <input type="radio" class="theme-checkbox" name="theme" @change="changeTheme('#E8E4E1')">
                        <span class="check"></span>
                    </li>
                </ul>
                <div class="theme-cta">
                    <button class="btn-main" :style="'background-color:'+this.newColor+''">
                        Done
                    </button>
                </div>
            </div>
            <div class="alert alert-success">
                <span class="alert-text">Successfully Change your Theme</span>
            </div>
            <div class="alert alert-error">
                <span class="alert-text">Successfully Change your Theme</span>
            </div>
            <div class="alert alert-warning">
                <span class="alert-text">Successfully Change your Theme</span>
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
import mainHeader from '~/components/Nav/header';
import mainMenu from '~/components/Nav/menu';
import themePicker from '~/components/Forms/themePicker';

export default {
    components: {
        mainHeader,
        mainMenu,
        themePicker
    },
    data() {
        return {
            settingsModal: false,
            newColor: ''
        }
    },
    methods:{
        showMenu() {
            this.settingsModal = true;
        },
        hideMenu() {
            this.settingsModal = false;
        },
        changeTheme(color){
            this.newColor = color;
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
a,button {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}
.alert {
    text-align:center;
    padding:10px;
    font-size:14px;
    border-radius:10px;
    letter-spacing: 0.4px;
}
.alert-success {
    color:#fff;
    background: green;
}
.alert-error {
    color:#fff;
    background-color: red;
}
.alert-warning {
    color:#222;
    background-color: #fff3cd;
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
    .theme-picker {
        background:#fff;
        padding:20px;
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
    }
    .theme-list {
        list-style-type: none;
        padding:0 0 20px;
        margin:0;
        display:flex;
        flex-wrap: wrap;
        width: 100%;
    }
    .theme-item {
        position:relative;
        width:60px;
        height:60px;
        margin:5px;
    }
    .theme-cta {
        text-align: center;
    }
    .btn-main {
        border:none;
        background-color:#0F4C75;
        color:#fff; 
        padding:10px 30px;
        font-size:14px;
        letter-spacing:0.4px;
        font-family: 'Roboto',sans-serif;
        border-radius:100px;
        outline:none;
        margin:0 auto;
    }
    .theme-checkbox {
        position:absolute;
        top:0;
        left:0;
        right:0;
        margin:0 auto;
        width:50px;
        height:50px;
        z-index:1;
        opacity:0;
    }   
    .check {
        position: absolute;
        top: 0;
        left: 0;
        right:0;
        margin:0 auto;
        height: 50px;
        width: 50px;
        background-color: #eee;
        border-radius:100px;
    }
    .theme-item:first-child .check {
        background-color: #BA7967;
    }
    .theme-item:nth-child(2) .check {
        background-color: #0F4C75;
    }
    .theme-item:nth-child(3) .check {
        background-color: #5E6F64;
    }
    .theme-item:nth-child(4) .check {
        background-color: #EEBB4D;
    }
    .theme-item:nth-child(5) .check {
        background-color: #BB3B0E;
    }
    .theme-item:nth-child(6) .check {
        background-color: #F08A5D;
    }
    .theme-item:nth-child(7) .check {
        background-color: #6EBFB5;
    }
    .theme-item:nth-child(8) .check {
        background-color: #FCCBCB;
    }
    .theme-item:nth-child(9) .check {
        background-color: #B134C6;
    }
    .theme-item:last-child .check {
        background-color: #E8E4E1;
    }
    .check:after {
        content:"";
        position:absolute;
        display:none;
    }
    .theme-checkbox:checked ~ .check:after {
        display:block;
    }
    .check:after {
        left: 0;
        right:0;
        margin:0 auto;
        top: 5px;
        width: 20px;
        height: 30px;
        border: solid white;
        border-width: 0 5px 5px 0;
        -webkit-transform: rotate(45deg);
        -ms-transform: rotate(45deg);
        transform: rotate(45deg);
    }
</style>