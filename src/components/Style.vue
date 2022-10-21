<template>
    <div>
        <div class="box" :style = "{
            backgroundColor: color,
            height: height +'rem',
            width: width +'rem',
        }">

        </div>
        <p>{{color}}</p>

        <input type="color" v-model = "color">
        <input type="range" name="" id="" v-model = "height">
        <input type="range" name="" id="" v-model = "width">
        
    </div>
</template>
<script>
    export default{
        data(){
        return{
            color: "",
            height: '',
            width: '',
            
        }
    }
    }

</script>
<style scoped>
.box{
    height: 50px;
    width: 50px;
    background-color: red;
    border: 2px solid;
}

</style>