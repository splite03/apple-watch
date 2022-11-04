<template>
    <div class="apple__with__header">
        <div alt="" :class="'apple__with__header__picture ' + className"></div>
        <h2 :class="'apple__with__header__header ' + fz" id="apple__with__header__header">{{headerTitle}}</h2>
        <a class="apple__with__header__link" href="">{{link}}</a>
    </div>
</template>
<script>
export default {
    props:['className', 'headerTitle','link', 'fz']
}
</script>
<style lang="scss">
.apple__with__header{
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 450px;
    padding: 0px 20px;

    .apple__with__header__picture{
        margin: 10px 0;
        background-size: cover;

        &.logo__watch__s7{
            background-image: url(@/assets/logo__watch__s7.png);
            width: 132px;
            height: 51px;
        }
        &.logo__watch__se{
            background-image: url(@/assets/logo-watch-se__soyna2pegxeq_large.png);
            width: 132px;
            height: 51px;
        }
        &.fitness__logo{
            background-image: url(@/assets/logo_fitness_plus__b7eq6fhq3cc2_large.png);
            width: 341px;
            height: 62px;
        }
        &.apple__one{
            background-image: url(@/assets/logo-apple-one__cwtz6e3tcscy_large.png);
            width: 317px;
            height: 100px;
        }
        &.logo__music{
            background-image: url(@/assets/logo-apple-music__d3g9jd3q6d26_large.png);
            width: 161px;
            height: 40px;
        }
    }
    .apple__with__header__header{
        text-align: center;
        margin: 10px 0;
    }
    .apple__with__header__link{
        margin: 10px 0;
    }
}
@media (max-width: 1150px) {
    .apple__with__header{
        padding: 0;

        .apple__with__header__header{
            max-width: 300px;
        }
        .apple__with__header__picture{
            
            &.logo__watch__s7{
                background-image: url(@/assets/max-width-1080/logo_watch_s7__dnxp9zoaom82_medium.png);
                width: 108px;
                height: 43px;
            }
            &.logo__watch__se{
                background-image: url(@/assets/max-width-1080/logo-watch-se__soyna2pegxeq_medium.png);
                width: 109px;
                height: 42px;
            }
            &.fitness__logo{
                background-image: url(@/assets/max-width-1080/logo_fitness_plus__b7eq6fhq3cc2_medium.png);
                width: 227px;
                height: 42px;
            }
            &.apple__one{
                background-image: url(@/assets/max-width-1080/logo-apple-one__cwtz6e3tcscy_medium.png);
                width: 184px;
                height: 59px;
            }
            &.logo__music{
                background-image: url(@/assets/max-width-1080/logo-apple-music__d3g9jd3q6d26_medium.png);
                width: 116px;
                height: 29px;
            }
        }
        .apple__with__header__header{
            font-size: 32px;
            
            &.fz32{
                font-size: 21px;
            }
        }
    }
}
@media (max-width: 767px) {
    .apple__with__header{
        padding: 0;

        .apple__with__header__header{
            max-width: 300px;
        }
        .apple__with__header__picture{
            
            &.logo__watch__s7{
                background-image: url(@/assets/max-width-1080/logo_watch_s7__dnxp9zoaom82_medium.png);
                width: 108px;
                height: 43px;
            }
            &.logo__watch__se{
                background-image: url(@/assets/max-width-1080/logo-watch-se__soyna2pegxeq_medium.png);
                width: 109px;
                height: 42px;
            }
            &.fitness__logo{
                background-image: url(@/assets/max-width-738/logo_fitness_plus__b7eq6fhq3cc2_small.jpg);
                width: 145px;
                height: 28px;
            }
            &.apple__one{
                background-image: url(@/assets/max-width-738/logo-apple-one__cwtz6e3tcscy_small.png);
                width: 84px;
                height: 28px;
            }
            &.logo__music{
                background-image: url(@/assets/max-width-738/logo-apple-music__d3g9jd3q6d26_small.png);
                width: 115px;
                height: 28px;
            }
        }
        .apple__with__header__header{
            font-size: 32px;
            
            &.fz32{
                font-size: 21px;
            }
        }
    }
}
</style>