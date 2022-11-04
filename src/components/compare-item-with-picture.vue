<template>
    <div :class="'compare__item__with__picture ' + area">
        <div :class="'compare__item__with__picture__picture ' + className" alt=""></div>
        <div class="compare__item__colors">
            <div class="compare__item__color midnight"></div>
            <div class="compare__item__color starlight"></div>
            <div class="compare__item__color green"></div>
            <div class="compare__item__color blue"></div>
            <div class="compare__item__color red"></div>
        </div>
        <h3 class="compare__item__with__picture__header">{{title}}</h3>
        <a href="">Подробнee ></a>
        
    </div>
</template>
<script>
export default {
    props:['className','title','area']
}
</script>
<style lang="scss">
.compare__item__with__picture { 
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-bottom: 1px solid rgb(203, 203, 203);
    padding-bottom: 20px;

    &.s7__1{
        grid-area: s7__1;
    }
    &.s3__1{
        grid-area: s3__1;
    }
    &.se__1{
        grid-area: se__1;
    }

    .compare__item__with__picture__picture{
        background-size: cover;
        margin:0 50px 30px;
        width: 203px;
        height: 240px;

        &.compare__s7{
            background-image: url(@/assets/compare_s7__dqi9jnwa4sq6_large.jpg);
        }
        &.compare__s3{
            background-image: url(@/assets/compare_s3__f6gqpfe5rdea_large.jpg);
            height: 251px;
        }
        &.compare__se{
            background-image: url(@/assets/compare_se__fjdos6x4rmmy_large.jpg);
        }
    }
    a{
        font-size: 17px;
        font-weight: 300;
    }

    .compare__item__colors { 
        display: flex;
        justify-content: center;
        align-items: center;

        .compare__item__color { 
            margin-right: 4px;
            height: 11px;
            width: 11px;
            border-radius: 50%;
        }
        .midnight { 
            background-color: #1a2530;
        }
        .starlight { 
            background-color: #ded6d1;
        }
        .green { 
            background-color: #36382b;
        }
        .blue { 
            background-color: #6e8eba;
        }
        .red { 
            background-color: #a91e3b;
        }
    }
    .compare__item__with__picture__header { 
        padding: 32px 0 26px;
    }
}
@media (max-width:1150px) {
    .compare__item__with__picture{

        .compare__item__with__picture__picture{
            width: 167px;
            height: 200px;
            margin: 0 30px 30px;
            &.compare__s7{
                background-image: url(@/assets/max-width-1080/compare_s7__dqi9jnwa4sq6_medium.jpg);
            }
            &.compare__s3{
                background-image: url(@/assets/max-width-1080/compare_s3__f6gqpfe5rdea_medium.jpg);
                height: 206px;
            }
            &.compare__se{
                background-image: url(@/assets/max-width-1080/compare_se__fjdos6x4rmmy_medium.jpg);
            }
        }
    }
}
@media (max-width:767px) {
    .compare__grid__wrapper{
        margin-bottom: 40px;
    }
    .compare__item__with__picture{

        .compare__item__with__picture__picture{
            margin: 0 0 30px;
            width: 130px;
            height: 152px;

            &.compare__s7{
                background-image: url(@/assets/max-width-738/compare_s7__dqi9jnwa4sq6_small.jpg);
            }
            &.compare__s3{
                background-image: url(@/assets/max-width-738/compare_se__fjdos6x4rmmy_small.jpg);
                height: 152px;
            }
            &.compare__se{
                background-image: url(@/assets/max-width-738/compare_s3__f6gqpfe5rdea_small_2x.jpg);
                height: 160px;
            }
        }
    }
}
</style>