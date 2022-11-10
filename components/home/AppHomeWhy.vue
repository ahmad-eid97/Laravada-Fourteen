<template>
  <section class="why">
      <div class="row justify-content-center">
          <h2>Why We Are Different</h2>
      </div>
        <div class="row">
            <div class="col-lg-3 col-sm-6 item">
                <h3>01.</h3>
                <h4>Quality</h4>
                <p>
                    Nullam arcu felis, tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
            <div class="col-lg-3 col-sm-6 item">
                <h3>02.</h3>
                <h4>Integrity</h4>
                <p>
                    Tristique eget malesuada sed arcu felis, viverra viverra at sapien at sapien. Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
            <div class="col-lg-3 col-sm-6 item">
                <h3>03.</h3>
                <h4>Innovations</h4>
                <p>
                    Nunc ut – for dictum purus lorem vel ante ac purus sollicitudin dictum ipsum eget ex convallis from dolor.
                </p>
            </div>
            <div class="col-lg-3 col-sm-6 item">
                <h3>04.</h3>
                <h4>Safety</h4>
                <p>
                    Lorem ipsum dolor, tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor suscipit dlavrida.
                </p>
            </div>
        </div>
        <div class="row m-0">

            <swiper :options="swiperOption" class="owl-carousel">
                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-001.png" alt="">
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-002.png" alt="">
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-004.png" alt="">
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-003.png" alt="">
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-007.png" alt="">
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-006.png" alt="">
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/l-005.png" alt="">
                </div>
                </swiper-slide>
            </swiper>

        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeWhy',
    data () {
        return {
        swiperOption: {
            loop: true,
            slidesPerView: 6,
            spaceBetween: 50,
            breakpoints: {
            // when window width is >= 320px
            100: {
                slidesPerView: 1,
                spaceBetween: 5,
            },
            // when window width is >= 480px
            480: {
                slidesPerView: 2,
                spaceBetween: 5,
            },
            // when window width is >= 640px
            640: {
                slidesPerView: 3,
                spaceBetween: 5,
            },
            992: {
                slidesPerView: 4,
                spaceBetween: 5,
            },
            1200: {
                slidesPerView: 6,
                spaceBetween: 5,
            },
            },
        },
        }
    }

}
</script>

<style>
    .why {
        padding: 65px 65px 35px;
    }
    .why h2 {
        clear: both;
        color: rgb(51, 53, 57);
        font-size: 34px;
        font-weight: 700;
        line-height: 44px;
        margin-bottom: 15px;
        position: relative;
        margin-bottom: 40px;
        text-align: center;
    }

    .why h2::after {
        content: '';
        height: 3px;
        background-color: rgb(225, 61, 58);
        width: 200px;
        position: absolute;
        bottom: -10px;
        left: calc(50% - 100px);
    }
    .why p {
        color: rgb(51, 53, 57);
        font-size: 20px;
        font-weight: 400;
        line-height: 32px;
        text-align: center;
        max-width: 750px;
        margin-bottom: 80px;
    }

    .why .item h3{
        color: rgba(173, 176, 182, 0.18);
        font-size: 100px;
        font-weight: 700;
        line-height: 110px;
        margin-bottom: 15px;
        text-align: left;
    }
    .why .item h4{
        color: rgb(51, 53, 57);
        font-size: 20px;
        font-weight: 700;
        line-height: 30px;
        margin-bottom: 15px;
        text-align: left;
    }
    .why .item p{
        color: rgb(120, 125, 133);
        font-size: 15px;
        font-weight: 400;
        line-height: 26px;
        text-align: left;
    }
    .why .slick-slider {
        background-color: #f7f7f8;
    }
    .why .slick-slide .item {
        padding: 15px;
    }
    .why .slick-prev {
        left: 0;
    }
    .why .slick-next {
        right: 0;
    }
    .why .slick-prev, .why .slick-next {
        width: 40px;
        height: 40px;
        z-index: 2;
    }
    .why .slick-prev::before, .why .slick-next::before {
        font-family: 'slick';
        font-size: 24px;
        line-height: 1;
        opacity: 0.75;
        color: #a7afb3;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
</style>