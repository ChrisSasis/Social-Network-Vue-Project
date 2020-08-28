<template>
    <div>
        <div class="post-holder">
            <div class="post-wrapper">
                <div class="post-content">
                    <div class="post-body">
                        Lorem
                    </div>
                    <div class="post-footer">
                        <strong class="post-user">@eliminate123</strong>
                        <span class="post-date">December 1, 2020</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "publicPostContent",
    // props: ['post','created']
}
</script>

<style scoped>
.post-holder {
    padding:10px 0px;
}
.post-wrapper {
    width:100%;
}
.post-content {
    background-color:#F9F9F9;
    border-radius:10px;
}
/* .post-creator ,
.post-date{
    display:inline-block;
    width:100%;
} */
.post-user, .post-date {
    display:inline-block;
}
.post-user {
    color:#636363;
    padding-right:10px;
}
.post-date {
    font-size:12px;
    color:#6D6D6D;
}
.post-body {
    padding:15px;
    font-size:16px;
    letter-spacing: 0.4px;
    line-height: 1.3125;
}
.post-footer {
    border-top:1px solid #F1F1F1;
    padding:10px 15px;
}
</style>