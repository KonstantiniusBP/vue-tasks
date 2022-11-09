<template>
    <numbersVue v-for="n in 10" :comp-number="n"/>
</template>


<script>
import numbersVue from './numbers.vue';
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

</style>
