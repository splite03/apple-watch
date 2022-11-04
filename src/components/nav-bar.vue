<template >
   <nav class="navbar">
        <div class="navbar__wrapper">
            <apple-ico :fills="'white'"></apple-ico>
            <div class="navbar__links">
                <a href="" class="navbar__link">О нас</a>
                <a href="" class="navbar__link">Watch</a>
                <a href="" class="navbar__link">Выбери свои</a>
                <a href="" class="navbar__link">Fitness+</a>
                <a href="" class="navbar__link">Почему Apple Watch?</a>
                <a href="" class="navbar__link">Аксессуары</a>
                <a href="" class="navbar__link">Доставка</a>
            </div>
            <div class="menu__button" @click="dropMenu()"></div>
            <div class="navbar__drop">
                <a href="" class="navbar__link">О нас</a>
                <a href="" class="navbar__link">Watch</a>
                <a href="" class="navbar__link">Выбери свои</a>
                <a href="" class="navbar__link">Fitness+</a>
                <a href="" class="navbar__link">Почему Apple Watch?</a>
                <a href="" class="navbar__link">Аксессуары</a>
                <a href="" class="navbar__link">Доставка</a>
            </div>
        </div>
    </nav>
</template>
<script>
import appleIco from './apple-svg.vue'

export default{
    components: { appleIco },
    computed:{
        navbarDrop(){
            return document.querySelector('.navbar__drop')
        },
        dropButton(){
            return document.querySelector('.menu__button')
        }
    },
    methods:{
        dropMenu(){
            if(this.navbarDrop.classList[1]){
                this.navbarDrop.classList.remove('menu__droped')
                this.dropButton.classList.remove('menu__opened')
            }else{
                this.navbarDrop.classList.add('menu__droped')
                this.dropButton.classList.add('menu__opened')
            }
        }
    }
}
</script>
<style lang="scss">
.navbar__drop{
    display: none;
}
.navbar {
    height: 50px;   
    background-color: rgb(57, 57, 57);
    width: 100vw;
    position: fixed;
    z-index: 40;

    .navbar__wrapper{
        display: flex;
        position: relative;
        justify-content: center;
        align-items: center;
        height: 100%;
        margin: 0 auto;

        .navbar__links{

            .navbar__link{
                text-decoration: none;
                font-size: 14px;
                font-weight: 300;
                color: rgba(255, 255, 255, 0.615);   
                margin: 0 20px;
                transition: all .15s ease-in-out;
                &:hover{
                    color: white;
                }
            }
        }
    }
}
@media (max-width:840px) {
    .navbar{
        height: 70px;
    }
    .navbar__links{
        display: none;
    }
    .menu__button{
        position: absolute;
        right: 30px;
        cursor: pointer;
        &::before{
            transition: rotate .3s ease-in-out,translate .3s ease-in-out;
            content: '';
            height: 3px;
            width: 40px;
            background-color: white;
            display: block;
            margin-bottom: 15px;
        }
        &::after{
            transition: rotate .3s ease-in-out,translate .3s ease-in-out;
            content: '';
            height: 3px;
            width: 40px;
            background-color: white;
            display: block;
        }
        &.menu__opened{
            &::before{
                rotate: 45deg;
                translate: 0 8px;
            }
            &::after{
                rotate: -45deg;
                translate: 0 -10px;
            }
            }
        }
    }
    .navbar__drop{
        position: fixed;
        top: 70px;
        left: 0;
        display: flex;
        background-color: #565656;
        align-items: center;
        flex-flow: column;
        width: 100vw;
        height: 0;
        overflow: hidden;
        transition: height 1s ease-in-out;

        &.menu__droped{
            height: calc(100vh - 25px);
            a{
                opacity: 1;
            }
        }
        a{
            transition: opacity .6s .1s ease-in-out;
            opacity: 0;
            color: white;
            padding: 16px;
            font-size: 30px;
            font-weight: 300;
            border-bottom: 1px dashed grey;
            width: 100%;
            text-align: center;
        }
    }
@media (max-width: 767px) {
    .navbar{
        height: 50px;
    }
    .navbar__drop{
        top: 50px;
    }
    .menu__button{

        &::before{
            width: 30px;
            margin-bottom: 10px;
        }
        &::after{
            width: 30px;
        }
        &.menu__opened{
            &::before{
                translate: 0 6px;
            }
            &::after{
                translate: 0 -7px;
            }
        }
    }
}
</style>