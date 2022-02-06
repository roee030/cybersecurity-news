<template>
 <button class="button_root">
     <span class="button_icon">{{icon}}</span>
     <span class="button_text">{{label}}</span>
     </button>

</template>

<script>
export default {
name: "Button",
props:{
    label:String,
    icon:String,
    }
}
</script>

<style>
.button_root{
    margin-left:212px;
    width: 147px;
    background-color:#123BFF;
    height:46px;
    color: white;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:10px;
    cursor:pointer;
}
.button_root:hover{
    opacity: 0.7;
}

.button_icon{
    font-size:22px;
    color: white;
    margin-right:12px;
}

.button_text{
    font-size:16px;
}
</style>