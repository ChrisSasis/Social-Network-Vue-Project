<template>
    <div>
        <!-- settings popup -->
        <div class="settings-modal modal">
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
    name: "settingsModal",
    data() {
        return {
            settingsModal: false
        }
    },
    methods:{
        hideMenu() {
            this.settingsModal = false;
        }
    },
}
</script>

<style scoped>
/* modal */
.modal {
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