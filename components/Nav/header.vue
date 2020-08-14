<template>
    <div class="header">
        <div class="header-logo">
            <a href="#" class="header-link">
                <img src="https://www.freepnglogos.com/uploads/spotify-logo-png/file-spotify-logo-png-4.png" alt="" class="header-img">
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "mainHeader"
}
</script>

<style scoped>
.header {
    padding:10px;
    box-shadow:0px 0px 4px rgba(0,0,0,0.1);
}
.header-logo {
    width:30px;
    margin:0 auto;
}
.header-link {
    display:block;
}
</style>