<template>
    <div class="row">
        <numbersVue v-for="n in numbersCount" :comp-number="n"/>
    </div>
</template>


<script>
import numbersVue from './numbers.vue';
export default{
    
    name:"user-data",
    data(){
            return{
                numbersCount: 1,
            }
    },
    props:{
    },
    methods:{
    },
    computed:{
    },
    components:{
        numbersVue
    }
}
</script>


<style scoped>
*{
    font-family: 'Montserrat', sans-serif;
}
.row{
    display: flex;
    flex-direction: row;

    gap: 10px;
}
</style>
