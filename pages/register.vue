<template>
    <div>
        <div class="logo">
            <div class="logo-holder">
                <img src="/icon.png" alt="">
            </div>
            <div class="title">ShoutSpace | Beta</div>
        </div>
        <div class="form-container">
            <div class="form-holder">
                <label for="username" class="form-label">Name</label>
                <input type="text" class="form-input" id="username">
            </div>
            <div class="form-holder">
                <label for="username" class="form-label">Email Address</label>
                <input type="text" class="form-input" id="username">
            </div>
            <div class="form-holder">
                <label for="username" class="form-label">Username</label>
                <input type="text" class="form-input" id="username">
            </div>
            <div class="form-holder">
                <label for="password" class="form-label">Password</label>
                <input type="password" class="form-input" id="password">
            </div>
            <div class="form-holder">
                <label for="password" class="form-label">Confirm Password</label>
                <input type="password" class="form-input" id="password">
            </div>
            <div class="form-holder">
                <button class="btn-main">Register</button>
            </div>
        </div>
        <div class="cta">
            <!-- <a href="#" class="bullet-right">Forgot Password?</a> -->
            <a href="/login">Login</a>
        </div>
        <div class="other-cta">
            <ul class="cta-list">
                <li>
                    <a href="#" class="cta-link">About Us</a>
                </li>
                <li>
                    <a href="#" class="cta-link">Privacy</a>
                </li>
                <li>
                    <a href="#" class="cta-link">Terms</a>
                </li>
                <li>
                    <a href="#" class="cta-link">Contact Us</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "register"
}
</script>
<style>
a,button{
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
img {
    width:100%;
}
.logo-holder {
    width:80px;
    margin: 0 auto;
}
.logo {
    text-align: center;
    padding:60px;
}
.title {
    font-family: 'Roboto',sans-serif;
    letter-spacing: 0.4px;
    padding-top:10px;
    font-weight: bold;
    font-size:20px;
}
.form-container {
    max-width:500px;
    margin:0 auto;
}
.form-holder {
    padding:15px 20px 20px;
}
.form-label {
    display:block;
    font-size:16px;
    font-family: 'Roboto',sans-serif;
    letter-spacing: 0.4px;
    font-weight: bold;
    cursor:pointer;
}
.form-input {
    margin-top:10px;
    display:block;
    font-size:16px;
    width:100%;
    padding:10px 0px;
    outline:none;
    border:none;
    border-bottom:1px solid #4058DB;
}
.btn-main {
    border:none;
    display:block;
    width:100%;
    padding:15px;
    font-size:18px;
    letter-spacing:0.4px;
    border-radius:100px;
    background-color: #206a5d;
    color:#fff;
    box-shadow:0px 3px 11px rgba(0,0,0,0.3);
    outline:none;
    cursor: pointer;
}
.cta {
    text-align:center;
    padding:10px 20px;
}
.cta a {
    color:#000;
    font-weight:bold;
    outline:none;
    padding:10px;
    display:block;
    text-decoration: none;
    position:relative;
    font-size:14px;
}
.other-cta {
    margin-top: 120px;
}
.bullet-right {
    position:relative;
    padding:10px;
}
.bullet-right:before {
    content:"";
    width:8px;
    height:8px;
    background: #DA8D8D;
    border-radius:100px;
    position:absolute;
    top:50%;
    right:-5px;
    transform:translateY(-50%);
}
.cta-list {
    list-style-type: none;
    padding:0;
    margin:0;
    display:flex;
    justify-content: center;
}
.cta-link {
    font-size:14px;
    text-decoration: none;
    display:block;
    color:#676767;
    padding:10px 15px;
}
</style>