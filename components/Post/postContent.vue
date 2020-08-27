<template>
    <div>
        <div class="post-holder">
            <div class="post-wrapper">
                <div class="post-content">
                    <div class="post-body">
                        <!-- {{post}} -->
                        Lorem
                    </div>
                    <div class="post-footer">
                        <!-- <span class="post-date">{{ $moment(created).format('LL') }}</span> -->
                        December 1, 2020
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "postContent",
    props: ['post','created']
}
</script>

<style scoped>
.post-holder {
    padding:10px 20px;
}
.post-wrapper {
    width:100%;
}
.post-content {
    background-color:#F9F9F9;
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