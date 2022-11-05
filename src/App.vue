<template>
  <nav-bar></nav-bar>
  <main>
    <div class="grey__background">
      <div class="picture__with__apple__comp">
        <apple-with-header 
        :className="'logo__watch__s7'"
        :headerTitle="'Показывают максимум.'"
        :link="'Подробнee >'"></apple-with-header>
        <div class="picture__with__apple__comp__picture" id="picture__with__apple__comp__picture"></div>
      </div>
      <div class="container">
        <div class="two__series__wrapper">
          <div class="two__series__picture picture__s7"></div>
          <div class="two__series__about">
            <h5>Apple Watch с самым большим дисплеем.</h5>
            <p>Более чем на 50% увеличена область просмотра по сравнению с Series 3.</p>
            <div class="two__series__picture picture__s7 picture__s7__mobile"></div>
            <div class="two__series__buttons-wrapper">
              <div class="two__series__slider two__series__slider__s7__active"></div>
              <div class="two__series__button two__series__button__active" @click="slide('s7')">Series 7</div>
              <div class="two__series__button" @click="slide('s3')">Series 3</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="watch__se">
      <div class="container">
        <div class="watch__se__wrapper">
          <apple-with-header
          :className="'logo__watch__se'"
          :headerTitle="'Мало не покажут.'"
          :link="'Подробнее >'"></apple-with-header>
          <div class="watch__se__picture" alt=""></div>
        </div>
      </div>
    </div>
    <div class="compare__block" id="compare">
      <div class="container">
        <div class="compare__block__wrapper">
          <h2 class="compare__header">Какие Apple Watch вам подходят?</h2>
          <div class="compare__grid__wrapper">
            <compare-item-with-picture
            :className="'compare__s7'"
            :title="'Apple Watch Series 7'"
            :area="'s7__1'"></compare-item-with-picture>
            <compare-item-with-picture
            :className="'compare__se'"
            :title="'Apple Watch Series SE'"
            :area="'s3__1'"></compare-item-with-picture>
            <compare-item-with-picture
            :className="'compare__s3'"
            :title="'Apple Watch Series 3'"
            :area="'se__1'"></compare-item-with-picture>
            <div class="compare__item s7__2" >
              <h4>Корпус 45 мм или 41 мм</h4>
              <p>Защита от воды при плавании</p>
              <p>Сверхпрочное фронтальное стекло с защитой от трещин</p>
              <p>Защита от пыли: рейтинг IP6X</p>
            </div>
            <div class="compare__item se__2" >
              <h4>Корпус 44 мм или 40 мм</h4>
              <p>Защита от воды при плавании</p>
              <p class="none none__small"></p>
              <p class="none none__small"></p>
            </div>
            <div class="compare__item s3__2" >
              <h4>Корпус 42 мм или 38 мм</h4>
              <p>Защита от воды при плавании</p>
              <p class="none none__small"></p>
              <p class="none none__small"></p>
            </div>
            <div class="compare__item s7__3" >
              <img src="@/assets/quicklook_retina_display_s7__euol4grkrx8i_large.png" alt="">
              <p>Всегда включённый дисплей Retina</p>
              <p class="grey__paragraf">По сравнению с Apple Watch SE увеличен примерно на 20</p>
              <p class="grey__paragraf">По сравнению с Series 3 увеличен более чем на 50%</p>
            </div>
            <div class="compare__item se__3" >
              <img src="@/assets/quicklook_retina_display_se__bkqpyec086ya_large.png" alt="">
              <p>Дисплей Retina</p>
              <p class="grey__paragraf">По сравнению с Series 3 увеличен более чем на 30%</p>
            </div>
            <div class="compare__item s3__3" >
              <img src="@/assets/quicklook_retina_display_s3__c28bwxqba1w2_large.png" alt="">
              <p>Дисплей Retina</p>
            </div>
            <div class="compare__item s7__4" >
              <img src="@/assets/quicklook_bo_app__bn0uz5oly82u_large.png" alt="">
              <p>Приложение «Кислород в крови»</p>
            </div>
            <div class="compare__item se__4" >
              <p class="none"></p>
            </div>
            <div class="compare__item s3__4" >
              <p class="none"></p>
            </div>
            <div class="compare__item s7__5" >
              <img src="@/assets/quicklook_ecg_app__cha5dfocq4wi_large.png" alt="">
              <p>Приложение «ЭКГ»</p>
            </div>
            <div class="compare__item se__5" >
              <p class="none"></p>
            </div>
            <div class="compare__item s3__5" >
              <p class="none"></p>
            </div>
            <div class="compare__item s7__6" >
              <img src="@/assets/quicklook_heart_rate_notifications__dwkylcnr0nu6_large.png" alt="">
              <p class="compare__item__heart">Уведомления о слишком низком и высоком пульсе</p>
              <p class="compare__item__heart">Уведомления о нерегулярном ритме сердца</p>
            </div>
            <div class="compare__item se__6" >
              <img src="@/assets/quicklook_heart_rate_notifications__dwkylcnr0nu6_large.png" alt="">
              <p class="compare__item__heart">Уведомления о слишком низком и высоком пульсе</p>
              <p class="compare__item__heart">Уведомления о нерегулярном ритме сердца</p>
            </div>
            <div class="compare__item s3__6" >
              <img src="@/assets/quicklook_heart_rate_notifications__dwkylcnr0nu6_large.png" alt="">
              <p class="compare__item__heart">Уведомления о слишком низком и высоком пульсе</p>
              <p class="compare__item__heart">Уведомления о нерегулярном ритме сердца</p>
            </div>
            <div class="compare__item compare__item__underline s7__7" >
              <img src="@/assets/quicklook_sos__eevzwecgdqaa_large.png" alt="">
              <p>Экстренный вызов — SOS</p>
              <p>Функция обнаружения падения</p>
            </div>
            <div class="compare__item compare__item__underline se__7" >
              <img src="@/assets/quicklook_sos__eevzwecgdqaa_large.png" alt="">
              <p>Экстренный вызов — SOS</p>
              <p>Функция обнаружения падения</p>
            </div>
            <div class="compare__item compare__item__underline s3__7" >
              <img src="@/assets/quicklook_sos__eevzwecgdqaa_large.png" alt="">
              <p>Экстренный вызов — SOS</p>
              <p class="none none__small"></p>
            </div>
          </div>
          <p>
            <a href="">Сравните все модели ></a>
          </p>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="watch__fitness__wrapper">
        <div class="watch__fitness__picture"></div>
        <apple-with-header
        :className="'fitness__logo'"
        :headerTitle="'Получите три месяца бесплатной подписки при покупке Apple Watch.'"
        :link="'Подробнее об Apple Fitness+'"
        :fz="'fz32'"></apple-with-header>
      </div>
    </div>
    <div class="why__watch">
      <div class="container">
        <div class="why__watch__wrapper">
          <div class="why__watch__item">
            <h3 class="why__watch__item__preheader">Почему Apple Watch</h3>
            <h2 class="why__watch__item__header">Это мощное устройство для здорового образа жизни.</h2>
            <a href="" class="why__watch__link">Подробнee ></a>
            <div class="why__watch__item__picture left__pic"></div>
          </div>
          <div class="why__watch__item">
            <h2 class="why__watch__item__header why__watch__right__header">Система watchOS 8</h2>
            <h4 class="why__watch__item__midline">Осознанно. Грандиозно.</h4>
            <a href="" class="why__watch__link">Узнайте подробности о новых возможностях  ></a>
            <div class="why__watch__item__picture right__pic"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="accessories">
      <div class="container">
        <div class="accessories__wrapper">
          <h1 class="accessories__headline">Аксессуары для Apple Watch</h1>
          <div class="accessories__item">
            <div class="accessories__item__content">
              <h2 class="accessories__item__header">Изящный стиль.</h2>
              <h2 class="accessories__item__header">Эффектный вид.</h2>
            </div>
            <div class="accessories__item__picture accessories__item__picture__right__left"></div>
          </div>
          <div class="accessories__item">
            <div class="accessories__item__content">
              <h2 class="accessories__item__header">Магия от и до.</h2>
              <h4 class="accessories__item__midline">Сравните все модели AirPods и выберите самые подходящие.</h4>
              <a href="" class="accessories__link">Подробнее ></a>
            </div>
            <div class="accessories__item__picture accessories__item__picture__right"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="delivery__block">
      <img src="@/assets/package-regular-108.png" alt="">
      <h3>Бесплатная доставка</h3>
      <h4>И бесплатный возврат.</h4>
      <h4>Сроки доставки можно узнать</h4>
      <h4>на странице оформления заказа.</h4>
      <a href="">Подробнee ></a>
    </div>
    <div class="other__grid">
      <div class="container">
        <div class="other__grid__wrapper">
          <h1>Как получить больше пользы от Apple Watch</h1>
          <div class="other__grid__item other__grid__item__upper">
            <div class="other__grid__item__picture other__grid__item__picture__first"></div>
            <div class="other__grid__item__upper__item">
              <apple-with-header
              :className="'apple__one'"
              ></apple-with-header>
              <h4 class="other__grid__item__header">До пяти сервисов Apple в одной подписке. Вместе выгоднее.</h4>
              <div class="other__grid__item__links">
                <a href="">Попробуйте бесплатно 🡥</a>
                <a href="">Подробнее ></a>
            </div>
            </div>
          </div>
          <div class="other__grid__item">
            <apple-with-header
            :className="'logo__music'"
            ></apple-with-header>
            <h4 class="">Более 90 миллионов треков. <br> Слушайте бесплатно прямо сейчас.</h4>
            <div class="other__grid__item__links">
              <a href="">Попробуйте бесплатно 🡥</a>
              <a href="">Подробнее ></a>
            </div>
            <div class="other__grid__item__picture other__grid__item__picture__bilash"></div>
          </div>
          <div class="other__grid__item other__grid__item__rings">
            <h2>Три кольца. Одна цель.</h2>
            <a href="">Как заказывать кольца активности <br> на Apple Watch ></a>
            <div class="other__grid__item__picture other__grid__item__picture__rings"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="health__block">
      <div class="container">
        <div class="health__block__wrapper">
          <h2 class="health__block__header">Приложение «Здоровье».</h2>
          <h3 class="health__block__midline">Со здоровой дозой обновлений.</h3>
          <a href="" class="health__block__link">Подробнee ></a>
          <div class="health__block__picture"></div>
        </div>
      </div>
    </div>
  </main>
  <footer class="footer">
    <div class="container">
      <p>Выбирайте и покупайте</p>
      <p>Сервисы</p>
      <p>Apple Store</p>
      <p>Для бизнеса</p>
      <p>Ценности Apple</p>
      <a href="" class="footer__link">Магазин</a>
      <a href="" class="footer__link">Apple Music</a>
      <a href="" class="footer__link">Варианты оплаты</a>
      <a href="" class="footer__link">Apple в бизнесе</a>
      <a href="" class="footer__link">Универсальный доступ</a>
      <a href="" class="footer__link">Mac</a>
      <a href="" class="footer__link">Apple TV+</a>
      <a href="" class="footer__link">Переработка устройств Apple</a>
      <p style="margin-top:10px">Для образования</p>
      <a href="" class="footer__link">Окружающая среда</a>
      <a href="" class="footer__link">iPad</a>
      <a href="" class="footer__link">Apple Fitness+</a>
      <a href="" class="footer__link">Состояние заказа</a>
      <a href="" class="footer__link">Apple в образовании</a>
      <a href="" class="footer__link">Конфиденциальность</a>
      <a href="" class="footer__link">iPhone</a>
      <a href="" class="footer__link">Apple Arcade</a>
      <a href="" class="footer__link">Помощь при покупке</a>
      <a href="" class="footer__link">Покупка и поддержка</a>
      <p>О компании Apple</p>
      <a href="" class="footer__link">Watch</a>
      <a href="" class="footer__link">iCloud</a>
      <a href="" class="footer__link">Купите для учёбы</a>
      <a href="" class="footer__link">Newsroom</a>
      <a href="" class="footer__link">AirPods</a>
      <a href="" class="footer__link">Apple One</a>
      <a href="" class="footer__link"></a>
      <a href="" class="footer__link"></a>
      <a href="" class="footer__link">Руководство Apple</a>
      <a href="" class="footer__link"></a>
      <a href="" class="footer__link"></a>
      <a href="" class="footer__link"></a>
      <a href="" class="footer__link"></a>
      <a href="" class="footer__link"></a>
    </div>
  </footer>
</template>

<script>
import navBar from '@/components/nav-bar.vue'
import appleWithHeader from '@/components/apple-with-header.vue'
import compareItemWithPicture from '@/components/compare-item-with-picture.vue'
import AppleSvg from './components/apple-svg.vue'
export default {
  name: 'App',
  components: {navBar,appleWithHeader, compareItemWithPicture, AppleSvg},
  computed:{
    slider(){
      return document.querySelector('.two__series__slider')
    },
    sliderButtonS3(){
      return document.querySelectorAll('.two__series__button')[1 ]
    },
    sliderButtonS7(){
      return document.querySelectorAll('.two__series__button')[0]
    },
    twoSeriesPicture() {
      return document.querySelectorAll('.two__series__picture')
    }
  },
  methods:{
    slide(item){
      try{
        switch(item){
          case 's7':
            console.log(this.sliderButtonS3);
            this.sliderButtonS3.classList.remove('two__series__button__active')
            this.slider.classList.remove('two__series__slider__s3__active')
            this.twoSeriesPicture[0].classList.remove('picture__s3')
            this.twoSeriesPicture[1].classList.remove('picture__s3')

            this.sliderButtonS7.classList.add('two__series__button__active')
            this.slider.classList.add('two__series__slider__s7__active')
            break
          case 's3':
            this.sliderButtonS7.classList.remove('two__series__button__active')
            this.slider.classList.remove('two__series__slider__s7__active')
            
            this.sliderButtonS3.classList.add('two__series__button__active')
            this.slider.classList.add('two__series__slider__s3__active')
            this.twoSeriesPicture[0].classList.add('picture__s3')
            this.twoSeriesPicture[1].classList.add('picture__s3')
            console.log('s3');
            break
        }
      }catch(e){
        console.log(e);
      }
    }
  },
  mounted(){
    const a = document.querySelectorAll('a')
    a.forEach(e => e.addEventListener('click',(event) => event.preventDefault()))
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;500&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Roboto', sans-serif;
  font-size: 16px;
  font-weight: 300;
  scroll-behavior:smooth;
}
body{
  width: 100vw;
  height: 100vh;
  overflow-x: hidden;
}
a{
  text-decoration: none;
  color: rgb(0, 154, 201);
  font-weight: 400;
  font-size: 20px;
}
h1, h2, h3, h4, h5{
  font-weight: bold;
  text-align: center;
  color: rgb(55, 55, 55);
}
h1{
  font-size: 58px;
}
h2{
  font-size: 48px;
}
h3{
  font-size: 21px;
}
h4{
  font-size: 19px;
}
h5{
  font-size: 17px;
}
img{
  pointer-events: none;
  -moz-user-select: none; 
  -webkit-user-select: none; 
  -ms-user-select: none; 
  user-select: none;
}
.container{
  width: 100%;
  height: 100%;
  max-width: 1400px;
  margin: 0 auto;
}
.grey__background{
  background-color: #f5f5f7;
  padding-bottom: 150px;
}
.picture__with__apple__comp{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 50px 0 100px;

  .picture__with__apple__comp__picture{
    margin: 20px 0;
    background-image: url(@/assets/hero_s7__ep2maoos292e_large.jpg);
    background-size: cover;
    width: 988px;
    height: 856px;
  }
}
.two__series__wrapper { 
  display: flex;
  justify-content: center;
  background-color: white;
  border-radius: 20px;
  padding: 130px 50px;

  .two__series__picture { 
    background-size: cover;
    background-repeat: no-repeat;
    width: 406px;
    height: 693px;
    margin-right: 20px;
    transition: background-image .7s ease-in-out;
  }
  .picture__s7 { 
    background-image: url(@/assets/display_s7__fj2bqp6brfiy_large.jpg);
  }
  .picture__s3 { 
    background-image: url(@/assets/display_s3__f9n138ohv7e6_large.jpg);
  }
  .two__series__about { 
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: 20px;

    .picture__s7__mobile{
      display: none;
    }
    h5{
      font-size: 18px;
      font-weight: normal;
      color: rgb(62, 62, 62);
    }
    p{
      font-size: 64px;
      font-weight: bold;
      text-align: start;
      max-width: 460px;
      background: linear-gradient(90deg,#79b588,#3e593f);
      -webkit-background-clip: text;
      -moz-background-clip: text;
      -webkit-text-fill-color: transparent;
      -moz-text-fill-color: transparent;
    }

    .two__series__buttons-wrapper { 
      position: relative;
      border-radius: 50px;
      background-color: #f5f5f7;
      display: flex;
      justify-self: flex-end;
      margin-top: auto;
      overflow: hidden;

      .two__series__slider { 
        position: absolute;
        top: 0;
        background: black;
        height: 100%;
        width: 50%;
        border-radius: 50px;
        transition: all .7s ease-in-out;
        &.two__series__slider__s7__active{
          left: 0;
        }
        &.two__series__slider__s3__active{
          left: calc(100% - 162.83px);
        }
      }
      .two__series__button { 
        position: relative;
        cursor: pointer;
        z-index: 10;
        font-size: 18px;
        font-weight: 300;
        transition: all .7s ease-in-out;
        padding: 20px 50px;
        &.two__series__button__active{
          color: white;
        }
      }
    }
    
  }
}
.watch__se{
  margin-top: 150px;

  .watch__se__wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #fafafa;
    padding: 130px 0;

    .watch__se__picture{
      margin-left: 50px;
      background-image: url(@/assets/tile-watch-se__knji2d25x8qe_large.jpg);
      background-size: cover;
      width: 579px;
      height: 534px;
    }
  }
}
.compare__block { 
  .compare__block__wrapper { 
    display: flex;
    flex-direction: column;
    align-items: center;
    .compare__header { 
      padding: 80px 0 40px;
      color: rgb(41, 41, 41);
    }
    .compare__grid__wrapper { 
      display: grid;
      grid-template-columns: repeat(3 ,1fr);
      grid-template-rows: repeat(8 ,auto);
      grid-row-gap: 44px;
      grid-column-gap: 32px;
      grid-template-areas: 's7__1 se__1 s3__1'
      's7__2 se__2 s3__2'
      's7__3 se__3 s3__3'
      's7__4 se__4 s3__4'
      's7__5 se__5 s3__5'
      's7__6 se__6 s3__6'
      's7__7 se__7 s3__7'
      ;

      .compare__item{
        display: flex;
        flex-direction: column;
        align-items: center;

        &.compare__item__underline{
          border-bottom: 1px solid rgb(203, 203, 203);
          padding-bottom: 40px;
        }
        .grey__paragraf{
          color: rgb(62, 62, 62);
          margin-top: 10px;
        }
        .compare__item__heart{
          max-width: 200px;
        }
        h4{
          color: rgb(74, 74, 74);
        }
        p{
          font-size: 14px;
          max-width: 250px;
          text-align: center;
          margin-top: 11px;
        }
        .none{
          width: 100%;
          height: 26px;
          position: relative;
          margin-top: 0;
          &::after{
            content: "";
            position: absolute;
            left: 50%;
            top: 50%;
            border-radius: 50px;
            transform: translate3d(-50%,-50%,0);
            width: 28px;
            height: 3px;
            background: #1d1d1f;
          }
          &.none__small{
            margin-top: 11px;
            
            &::after{
              width: 6px;
              height: 1px;
            }
          }
        }
        // &.s7__1{grid-area: s7__1;}
        &.s7__2{grid-area: s7__2;}
        &.s7__3{grid-area: s7__3;}
        &.s7__4{grid-area: s7__4;}
        &.s7__5{grid-area: s7__5;}
        &.s7__6{grid-area: s7__6;}
        &.s7__7{grid-area: s7__7;}
        // &.se__1{grid-area: s7__1;}
        &.se__2{grid-area: se__2;}
        &.se__3{grid-area: se__3;}
        &.se__4{grid-area: se__4;}
        &.se__5{grid-area: se__5;}
        &.se__6{grid-area: se__6;}
        &.se__7{grid-area: se__7;}
        // &.s3__1{grid-area: s7__1;}
        &.s3__2{grid-area: s3__2;}
        &.s3__3{grid-area: s3__3;}
        &.s3__4{grid-area: s3__4;}
        &.s3__5{grid-area: s3__5;}
        &.s3__6{grid-area: s3__6;}
        &.s3__7{grid-area: s3__7;}
      }
    }
  }
}
.watch__fitness__wrapper{
  margin-top: 200px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  position: relative;
  overflow: hidden;
  background-image: url(@/assets/fitness_plus__fl5ioto4a4eq_large.jpg);
  background-size: 1385px 852px;
  background-repeat: no-repeat;
  min-height: 852px;
  padding-right: 100px;
}
.fz32{
  font-size: 32px;
}
.why__watch { 
  margin-top: 200px;

  .why__watch__wrapper { 
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-column-gap: 30px;
    grid-row-gap: 30px;

    .why__watch__item { 
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      background-color: #fafafa;
      .why__watch__item__preheader { 
        margin-top: 80px;
        color: rgb(55, 55, 55);
        font-weight: 400;
      }
      .why__watch__item__header { 
        color:rgb(55,55,55);
        padding: 10px 0;
        max-width: 350px;
        text-align: center;
        &.why__watch__right__header{
          padding-top: 110px;
        }
      }
      .why__watch__item__midline { 
        padding-bottom: 20px;
      }
      .why__watch__link { 
        margin-bottom: 100px;
        max-width: 250px;
        text-align: center;
      }
      .why__watch__item__picture { 
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        position: relative;
        width: 100%;

        &.left__pic{
          background-image: url(@/assets/tile_why_watch__bzxlfokkvj36_large.jpg);
          height: 543px;
        }
        &.right__pic{
          background-image: url(@/assets/tile_watchos__fo0tafi6nn6u_large.jpg);
          height: 545px;
          justify-self: flex-end;
          margin-top: auto;
        }
      }
    }
  }
}
.accessories { 
  margin-top: 200px;
  .accessories__wrapper { 
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-column-gap: 30px;
    grid-row-gap: 30px;
    .accessories__headline { 
      margin-bottom: 100px;
      grid-column: span 2;
      text-align: center;
    }
    .accessories__item { 
      display: flex;
      flex-flow: column;
      justify-content: flex-start;
      align-items: center;
      background-color: rgb(250 250 250);
      .accessories__item__content{
        padding: 60px 40px;
        display: flex;
        flex-flow: column;
        align-items: center;
        position: relative;
        z-index: 10;
        .accessories__item__header { 
          color: rgb(55, 55, 55); 
        }
        .accessories__item__midline { 
          max-width: 300px;
          margin: 20px 0;
          font-weight: 300;
          text-align: center;
        }
        .accessories__link { }
      }
      .accessories__item__picture { 
          background-size: cover;
          background-repeat: no-repeat;
          background-position: center;
          position: relative;
          width: 100%;
          justify-self: flex-end;
          margin-top: auto;
        }
        .accessories__item__picture__right__left { 
          background-image: url(@/assets/tile_bands__4x5zbcsqc1ua_large.jpg);
          height: 427px;
        }
        .accessories__item__picture__right { 
          background-image: url(@/assets/airpods__cldonwj5wwya_large.jpg);
          height: 498px;
          margin-bottom: -100px;
          top: -100px;
        }
    }
  }
}
.delivery__block{
  display: flex;
  flex-flow: column;
  align-items: center;
  padding: 100px 0 140px;
  h4,h3{
    color: rgb(55, 55, 55);
    cursor: pointer;
  }
  h3{
    margin: 20px 0 10px;
  }
  h4{
    font-weight: 300;
    padding: 2px;
  }
  a{
    margin-top: 40px;
  }
}
.other__grid { 

  .other__grid__wrapper { 
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-column-gap: 30px;
    grid-row-gap: 30px;

    h1{
      grid-column: span 2;
    }
    .other__grid__item { 
      display: flex;
      flex-flow: column;
      align-items: center;
      justify-content: flex-start;
      background-color: #fafafa;
      padding-top: 75px;
      h4{
        font-weight: 400;
        color: rgb(55,55,55);
        margin-bottom: 15px;
        margin-top: -25px;
      }
      
      &.other__grid__item__upper { 
        grid-column: span 2;
        display: flex;
        flex-flow: row;
        justify-content: center;
        align-items: center;
        background-color: #fafafa;
        padding: 50px;
        flex: 1;
        .other__grid__item__upper__item{
          flex: 1;
          display: flex;
          flex-flow: column;
          align-items: center;
          justify-content: center;
        }
      }
      &.other__grid__item__rings{
        background-color: black;

        h2{
          color: white;
          margin-bottom: 20px;
        }
        a{
          margin-bottom: 50px;
          text-align: center;
        }
      }
      .other__grid__item__picture { 
        background-repeat: no-repeat;
        background-position: left;
        
        &.other__grid__item__picture__bilash{
          background-image: url(@/assets/bilash-airpods.jpg);
          height: 441px;
          width: 100%;
          background-size: 675px 441px;
          background-position: center;
        }
        &.other__grid__item__picture__first { 
          background-image: url(@/assets/tile_apple_one__dv857y6v8dyu_large.jpg);
          flex: 1;
          width: 542px;
          height: 329px;
          background-size: 542px 329px;
        }
        &.other__grid__item__picture__rings{
          background-image: url(@/assets/tile_rings__b6fsb8eh4j36_large.jpg);
          width: 379px;
          height: 382px;
          background-size: 379px 382px;
        }
      }
      .other__grid__item__header { 
        max-width: 280px;
        color: rgb(55, 55, 55);
        font-size: 24px;
        margin-bottom: 20px;
      }
      .other__grid__item__links {
        display: flex; 
        justify-content: center;
        align-items: center;
        a{
          margin-right: 20px;
          padding-bottom: 20px;
        }
      }
    }
  }
}
.health__block { 
  margin-top: 200px;
  .health__block__wrapper { 
    padding-top: 50px;
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    background-color: #fafafa;

    .health__block__header { 
      color: rgb(55, 55, 55);
      margin-bottom: 20px;
    }
    .health__block__midline { 
      color: rgb(113, 113, 113);
      margin-bottom: 20px;
    }
    .health__block__link { 
      margin-bottom: 40px;
    }
    .health__block__picture { 
      background-image: url(@/assets/tile_health__exde7a2pwjau_large.jpg);
      background-position: center;
      background-size: cover;
      height: 371px;
      width: 100%;
    }
  }
}
.footer{
  background-color: #dadada;
  .container{
    background-color: #dadada;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(8, 1fr);
    padding: 50px 50px;
    p{
      font-size: 12px;
      color: black;
      font-weight: 400;
      padding: 4px 0;
    }
    .footer__link{
      color: rgb(73, 73, 73);
      font-size: 12px;
      padding: 4px 0;
      &:hover{
        color: rgb(133, 133, 133);
      }
    }
  }
}
@media (max-width: 1150px) {
  .container{
    max-width: 700px;
  }
  h1,h2{
    font-size: 36px;
  }
  h3, h4{
    font-size: 17px;
  }
  a{
    font-size: 17px;
  }
  .watch__fitness__wrapper{
    padding-right: 20px;
  }
  .picture__with__apple__comp{
    padding-top: 100px;
  }
  #picture__with__apple__comp__picture{
    background-image: url(@/assets/max-width-1080/hero_s7__ep2maoos292e_medium.jpg);
    width: 654px;
    height: 566px;
  }
  .two__series__wrapper{
    padding: 50px 20px;
    .two__series__picture{
      &.picture__s7{
        background-image: url(@/assets/max-width-1080/display_s7__fj2bqp6brfiy_medium.jpg);
        height: 417px;
        width:242px;
      }
      &.picture__s3{
        background-image: url(@/assets/max-width-1080/display_s3__f9n138ohv7e6_medium.jpg);
        height: 417px;
        width:242px;
      }
    }
    .two__series__about {
      h5{
        text-align: start;
      }
      p{
        font-size: 48px;
        max-width: 350px;
        margin-bottom: 100px;
      }
    }
  } 
  .grey__background{
    padding-bottom: 70px;
  }
  .watch__se{
    margin-top: 70px;
    .watch__se__wrapper{
      padding: 55px 0;
      .watch__se__picture{
        background-image: url(@/assets/tile-watch-se__knji2d25x8qe_large.jpg);
        width: 358px;
        height: 330px;
        margin-left: 0;
      }
    }
  }
  .compare__block{
  
    .compare__block__wrapper{
      
      .compare__grid__wrapper{
        grid-column-gap: 10px;
      }
    }
  }
  .watch__fitness__wrapper{
    background-image: url(@/assets/max-width-1080/fitness_plus__fl5ioto4a4eq_medium.jpg);
    background-position-x: -150px;
    background-size: cover;
    margin-top: 100px;
    width: 100%;
    height: 450px;
    min-height: 0;
  }
  .why__watch{
    margin-top: 70px;

    .why__watch__wrapper{

      .why__watch__item{
        .why__watch__item__picture { 

          &.left__pic{
            background-image: url(@/assets/max-width-1080/tile_why_watch__bzxlfokkvj36_medium.jpg);
            height: 350px;
          }
          &.right__pic{
            background-image: url(@/assets/max-width-1080/tile_watchos__fo0tafi6nn6u_medium.jpg);
            height: 330px;
          }
        }
        .why__watch__item__header{
          max-width: 300px;
        }
      }
    }
  }
  .accessories {
    margin-top: 80px;
    .accessories__wrapper{
      .accessories__headline{
        margin-bottom: 70px;
      }
      .accessories__item{
        .accessories__item__content{
          padding: 60px 20px;
        }
        .accessories__item__picture__right__left{
          background-image: url(@/assets/max-width-1080/tile_bands__4x5zbcsqc1ua_medium.jpg);
          height: 290px;
          margin-top: 0;
        }
        .accessories__item__picture__right{
          background-image: url(@/assets/max-width-1080/airpods__cldonwj5wwya_medium.jpg);
          height: 282px;
        }
      }
    }
  }
  .other__grid{
    .other__grid__wrapper{
      .other__grid__item{
        &.other__grid__item__rings{
          h2{
            max-width: 289px;
          }
        }
        &.other__grid__item__upper{
          padding: 30px;
        }
        .other__grid__item__picture{
          &.other__grid__item__picture__first{
            background-size: cover;
            background-image: url(@/assets/max-width-1080/tile_apple_one__dv857y6v8dyu_medium.jpg);
            height: 191px;
          }
          &.other__grid__item__picture__bilash { 
            background-image: url(@/assets/bilash-airpods.jpg);
            background-size: cover;
            height: 289px;
            justify-self: flex-end;
            margin-top: auto;
          }
          &.other__grid__item__picture__rings{
            background-size: cover;
            background-image: url(@/assets/max-width-1080/tile_rings__b6fsb8eh4j36_medium.jpg);
            height: 279px;
            width: 277px;
            margin-bottom: 30px;
          }
        }
        .other__grid__item__links{
          flex-flow: column;
          a{
            padding-bottom: 6px;
          }
        }
      }
    }
  }
  .delivery__block{
    padding: 60px 0;
  }
  .health__block{
    margin-top: 30px;

    .health__block__wrapper{
      .health__block__picture{
        background-image: url(@/assets/max-width-1080/tile_health__exde7a2pwjau_medium.jpg);
        height: 263px;
      }
    }
  }
  
}
@media (max-width: 767px) {
  .container{
    max-width: none;
  }
  h1,h2{
    font-size: 36px;
  }
  h3, h4{
    font-size: 17px;
  }
  a{
    font-size: 17px;
  }
  .watch__fitness__wrapper{
    padding-right: 20px;
  }
  .picture__with__apple__comp{
    padding-top: 60px;
  }
  #picture__with__apple__comp__picture{
    background-image: url(@/assets/max-width-738/hero_s7__ep2maoos292e_small.jpg);
    background-position: center;
    width: 100%;
    max-width: 635px;
    height: 530px;
  }
  .two__series__wrapper{
    padding: 50px 20px;
    margin: 0 10px;
    flex-flow: column;
    align-items: center;

    .two__series__picture{
      display: none;

      &.picture__s7{
        background-image: url(@/assets/max-width-1080/display_s7__fj2bqp6brfiy_medium.jpg);
        height: 417px;
        width:242px;
      }
      &.picture__s3{
        background-image: url(@/assets/max-width-1080/display_s3__f9n138ohv7e6_medium.jpg);
        height: 417px;
        width:242px;
      }
    }
    .two__series__about {

      .picture__s7__mobile{
        display: block;
        margin-right: 0;
        align-self: center;
        margin-bottom: 20px;
      }
      h5{
        text-align: start;
        max-width: 200px;
        margin-bottom: 15px;
      }
      p{
        font-size: 29px;
        max-width: 270px;
        margin-bottom: 10px;
      }
      .two__series__buttons-wrapper{

        .two__series__button{
          padding: 20px 40px;
          font-size: 16px;
        }
        .two__series__slider{
          &.two__series__slider__s3__active{
            left: calc(100% - 134.84px);
          }
        }
      }
    }
  } 
  .watch__se{

    .watch__se__wrapper{
      flex-flow: column-reverse;

      .watch__se__picture{
        background-image: url(@/assets/max-width-738/tile-watch-se__knji2d25x8qe_small.jpg);
        width: 342px;
        height: 316px;
        margin-left: 0;
      }
    }
  }
  .compare__block{
    margin: 0 10px;
    .compare__block__wrapper{
      
      .compare__grid__wrapper{
        grid-template-columns: repeat(2, 1fr);
        grid-column-gap: 10px;
        grid-template-areas: 's7__1 se__1'
        's7__2 se__2'
        's7__3 se__3'
        's7__4 se__4'
        's7__5 se__5'
        's7__6 se__6'
        's7__7 se__7'
        's3__1 .'
        's3__2 .'
        's3__3 .'
        's3__4 .'
        's3__5 .'
        's3__6 .'
        's3__7 .';
      }
    }
  }
  .watch__fitness__wrapper{
    background-image: none;
    flex-flow: column;
    height: unset;
    margin-top: 40px;

    .watch__fitness__picture{
      background-image: url(@/assets/max-width-738/fitness_plus__fl5ioto4a4eq_small.jpg);
      background-position-x: 0;
      background-size: cover;
      margin-top: 0;
      margin-bottom: 20px;
      width: 421px;
      height: 279px;
      min-height: 0;
    }
  }
  .why__watch{
    margin-top: 70px;

    .why__watch__wrapper{
      display: flex;
      flex-flow: column;
      .why__watch__item{
        .why__watch__item__picture { 

          &.left__pic{
            background-image: url(@/assets/max-width-1080/tile_why_watch__bzxlfokkvj36_medium.jpg);
            height: 350px;
          }
          &.right__pic{
            background-image: url(@/assets/max-width-1080/tile_watchos__fo0tafi6nn6u_medium.jpg);
            height: 330px;
          }
        }
        .why__watch__item__header{
          max-width: 300px;
        }
      }
    }
  }
  .accessories {
    margin-top: 80px;
    .accessories__wrapper{
      display: flex;
      flex-flow: column;
      .accessories__headline{
        margin-bottom: 20px;
      }
      .accessories__item{
        .accessories__item__content{
          padding: 60px 20px;
        }
        .accessories__item__picture__right__left{
          background-image: url(@/assets/max-width-738/tile_bands__4x5zbcsqc1ua_small.jpg);
          height: 290px;
        }
        .accessories__item__picture__right{
          background-image: url(@/assets/max-width-738/airpods__cldonwj5wwya_small.jpg);
          height: 295px;
        }
      }
    }
  }
  .other__grid{
    .other__grid__wrapper{
      display: flex;
      flex-flow: column;
      align-items: center;

      h1{
        max-width: 270px;
      }
      .other__grid__item{
        width: 100%;
        padding-top: 40px;
        &.other__grid__item__rings{
          h2{
            max-width: 289px;
          }
        }
        &.other__grid__item__upper{
          flex-flow: column;
        }
        .other__grid__item__picture{
          &.other__grid__item__picture__first{
            background-size: cover;
            background-image: url(@/assets/max-width-738/tile_apple_one__dv857y6v8dyu_small.jpg);
            margin-left: 24px;
            height: 181px;
            width: 297px;
            flex: unset;
          }
          &.other__grid__item__picture__bilash { 
            background-image: url(@/assets/bilash-airpods.jpg);
            background-size: cover;
            height: 289px;
            justify-self: flex-end;
            margin-top: auto;
          }
          &.other__grid__item__picture__rings{
            background-size: cover;
            background-image: url(@/assets/max-width-738/tile_rings__b6fsb8eh4j36_small.jpg);
            width: 263px;
            height: 263px;
            margin-bottom: 30px;
          }
        }
        .other__grid__item__links{
          flex-flow: column;
          a{
            padding-bottom: 6px;
            margin-right: 0;
          }
        }
      }
    }
  }
  .delivery__block{
    padding: 60px 0;
  }
  .health__block{
    margin-top: 30px;

    .health__block__wrapper{
      .health__block__picture{
        background-image: url(@/assets/max-width-738/tile_health__exde7a2pwjau_small.jpg);
        height: 263px;
      }
    }
  }
  .footer{
    .container{
      padding: 50px 10px;
      a,p{
        font-size: 11px;
        max-width: 50px;
      }
    }
  }
}
</style>
