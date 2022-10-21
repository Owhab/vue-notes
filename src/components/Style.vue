<template>
    <div>
        <div class="box" :style = "{
            backgroundColor: color,
        }">

        </div>
        <p>{{color}}</p>

        <input type="color" v-model = "color">
        
    </div>
</template>
<script>
    export default{
        data(){
        return{
            color: "#000",
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