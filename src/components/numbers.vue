<template>
    <div class="container">
        <div class="elem">
            <div class="elem1">{{compNumber}}</div>
            <div class="elem2">
                <input type="number" placeholder="0">
            </div>
        </div>
    </div>
</template>


<script>
// import numbersRow from './numbersRow.vue';
export default{
    name:"user-data",
    data(){
            return{
            }
    },
    props:{
        img: String,
        title: String,
        options: Array,

        compNumber: {
            type: Number,
            default: 1
        },

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
.container:last-child .elem1{
    background: #B3A9E3;
}
.elem{
    display: flex;
    flex-direction: row;
}
.elem1{
    display: flex;
    justify-content: center;
    width: 44px;
    height: 50px;

    font-weight: 800;
    font-size: 18px;
    color: #FFFFFF;

    align-items: center;
    background: #7F3BD6;
    border-radius: 3px 0px 0px 3px;
}

.elem2{
    display: flex;
    justify-content: center;
    width: 44px;
    height: 50px;

    font-weight: 800;
    font-size: 18px;
    color: #938F97;

    align-items: center;

    background: #EBEEF4;
    border-radius: 3px 0px 0px 3px;
}
.elem2 input{
    width: 44px;
    height: 50px;
    background: none;
    border: none;
}

</style>
