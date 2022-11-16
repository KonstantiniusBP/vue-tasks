<template>
    <input type="checkbox" class="checkbox" id="checkbox">
    <label for="checkbox" class="switcher-medium" :class="{medium: type == 'switcher-medium', small: type == 'switcher-small'}">
        <div class="switcher-circle-medium" :class="{medium: type == 'switcher-circle-medium', small: type == 'switcher-circle-small'}"></div>
    </label>
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
        isDisabled: Boolean
    },
    methods:{
    },
    computed:{
    },
    components:{
    }
}
</script>


<style scoped>
*{
    font-family: 'Montserrat', sans-serif;
}

.checkbox:checked + .switcher-medium{
    display: flex;
    width: 51px;
    height: 30px;

    justify-content: end;

    background: #EC458B;
    border-radius: 45px;

    align-items: center;
    padding-left: 4px;
    padding-right: 4px;
}

.switcher-medium{
    display: flex;
    width: 51px;
    height: 30px;

    background: #BACAD7;
    border-radius: 45px;

    align-items: center;
    padding-left: 4px;
}
.switcher-circle-medium{
    display: flex;
    justify-content: start;
    width: 22px;
    height: 22px;

    background: #FFFFFF;
    border-radius: 24px;
}
.switcher-small{
    display: inline-block;
    width: 40px;
    height: 24px;

    background: #EC458B;
    border-radius: 45px;
}

.switcher-circle-small{
    display: flex;
    justify-content: start;
    width: 17px;
    height: 17px;

    background: #FFFFFF;
    border-radius: 24px;
}


.checkbox:checked + .switcher-small{
    display: flex;
    width: 51px;
    height: 30px;

    justify-content: end;

    background: #EC458B;
    border-radius: 45px;

    align-items: center;
    padding-left: 4px;
    padding-right: 4px;
}


#checkbox{
    display: none;
}
</style>
