<template>
    <div class="container">
        <div class="upper-part" @click="dropdownFunc">
            <div class="upper-part-container">
                <div class="upper-part__img">
                    <img :src="'src/assets/images/' + img" alt="">
                </div>
                <div class="upper-part__title">
                    <p>{{title}}</p>
                </div>
            </div>
            <img src="../assets/images/Up.svg" alt="" class="upper-part__image_class " :class="{'upper-part__image_class-active': isOpen}">
        </div>
        <div class="dropdown-part" :hidden="!isOpen">
            <div class="dropdown-part__elem" v-for="item in options">
                <p>{{item}}</p>
            </div>
        </div>
    </div>
</template>


<script>
export default{
    name:"user-data",
    data(){
            return{
                isOpen: false,
            }
    },
    props:{
        img: String,
        title: String,
        options: Array,
    },
    methods:{
        dropdownFunc(){
            console.log('///////////////')
            console.log(this.isOpen)
            this.isOpen = !this.isOpen
        }
    },
    computed:{
    }
}
</script>


<style>
*{
    font-family: 'Montserrat', sans-serif;
}
body{
    background: rgb(68, 68, 68);
}
.container{
    overflow: hidden;
    width: 242px;
}

.upper-part{
    display: flex;
    justify-content: space-between;

    border-radius: 8px;
    background: #F2FAE9;
}

.upper-part-container{
    display: flex;
    flex-direction: row;

    gap: 18px;

    font-weight: 700;
    font-size: 16px;
    color: #8BD32E;

    text-align: center;
    align-items: center;
}

.upper-part__image_class{
    padding-right: 8px;
}
.upper-part__image_class-active{
    rotate: 180deg;
}

.dropdown-part{
    border-radius: 8px;
    background: #F6F8F5;

    transition: 1s;
}

.dropdown-part__elem{
    font-weight: 400;
    font-size: 14px;
    padding-top: 14px;
    padding-bottom: 14px;
    padding-left: 56px;
}
</style>
