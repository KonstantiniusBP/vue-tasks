<template>
    <div class="container">
        <div class="radiobuttons-class">
            <input type="radio" name="radio" id="radio1">
            <label for="radio1">25</label>
            <input type="radio" name="radio" id="radio2">
            <label for="radio2">50</label>
            <input type="radio" name="radio" id="radio3">
            <label for="radio3">100</label>
            <input type="radio" name="radio" id="radio4">
            <label for="radio4">200</label>
        </div>
    </div>
</template>


<script>
export default{
    name:"user-data",
    data(){
            return{

            }
    },
    props:{

    },
    methods:{
    },
    computed:{
    }
}
</script>


<style scoped>
*{
    font-family: 'Montserrat', sans-serif;
}
.radiobuttons-class{
    display: flex;
    width: 408px;
    overflow: hidden;
    border-radius: 3px;
}
.radiobuttons-class input{
    display: none;
}
.radiobuttons-class label{
    display: flex;
    width: 102px;
    height: 62px;
    align-items: center;
    justify-content: center;
    color: white;
    background: #5377D2;
}
.radiobuttons-class input:checked + label{
    background: #3A5EBC;
}
</style>
