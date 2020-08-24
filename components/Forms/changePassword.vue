<template>
    <div class="edit-profile-form"> 
        <div class="form-holder">
            <label for="" class="form-label">New Password</label>
            <input type="password" class="form-input">
        </div>
        <div class="form-holder">
            <label for="" class="form-label">Confirm Password</label>
            <input type="password" class="form-input">
        </div>
        <div class="form-holder">
            <button class="btn btn-primary">Save</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "changePassword"
}
</script>

<style>
.edit-profile-form {
    background: #fff;
    padding:20px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}
.form-label {
    font-size:16px;
    font-weight:bold;
}
.form-holder {
    padding-bottom:20px;
}
.form-input {
    display:block;
    width:100%;
    margin-top:10px;
    padding:10px 0px;
    font-size:16px;
    border:none;
    border-bottom:1px solid #0F4C75;
    outline:none;
}
.btn {
    border:none;
    background-color:#0F4C75;
    color:#fff; 
    padding:10px 30px;
    font-size:14px;
    letter-spacing:0.4px;
    font-family: 'Roboto',sans-serif;
    border-radius:100px;
    outline:none;
}
</style>