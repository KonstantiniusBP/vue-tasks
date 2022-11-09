<template>
    <div class="image-block">
        <img :src="imgsrc" alt="" v-if="(imgsrc)">
        <p v-else>{{initialsFunc}}</p>
        <div class="image-block__new-image">
            <label for="input-file" class="label-class">Изменить фото</label>
            <input type="file" id="input-file" ref="input_file" @change="upload_photo">
        </div>
    </div>
</template>


<script>
export default{
    name:"user-data",
    data(){
            return{
                user_photo: null,
                imgsrc: null,
            }
    },
    props:{
        username: String,
    },
    methods:{
        upload_photo(){
            this.user_photo = this.$refs.input_file.files[0];
            console.log(this.user_photo)
            const reader = new FileReader()
            reader.readAsDataURL(this.user_photo)
            reader.onload = () => (this.imgsrc = reader.result)
        }
    },
    computed:{
        initialsFunc(){
            let fullname = this.username.split(' ');
            let initials = (fullname.shift().charAt(0) + fullname.pop().charAt(0)).toUpperCase()
            return initials
        }
    }
}
</script>


<style scoped>
.image-block{
    position: relative;
    width: 124px;
    height: 124px;
    background: #D1D1D1;
    border-radius: 20px;
    overflow: hidden;
}
.image-block img{
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.image-block p{
    font-family: 'Montserrat', sans-serif;
    font-size: 44px;
    text-align: center;
}

#input-file{
    display: none;
}
.label-class{
    display: inline-block;
    position: absolute;
    width: 124px;

    bottom: -47px;
    text-align: center;
    border: 1px solid red;
    background: rgba(0, 0, 0, 0.5);

    font-size: 16px;
    padding-top: 13px;
    padding-bottom: 14px;
    font-weight: 400;
    color: #ffff;

    transition: 1s;
}
.image-block:hover .label-class{
    bottom: 0;
    transition: 1s;
}
</style>
