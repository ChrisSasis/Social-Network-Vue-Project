<template>
    <div class="theme-picker">
        <ul class="theme-list">
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme" checked>
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
            <li class="theme-item">
                <input type="radio" class="theme-checkbox" name="theme">
                <span class="check"></span>
            </li>
        </ul>
        <div class="cta">
            <button class="btn-main">
                Done
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: "themePicker"
}
</script>

<style scoped>
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
.cta {
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