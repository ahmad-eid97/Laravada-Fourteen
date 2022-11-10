<template>
    <section class="team">
        <div class="row justify-content-center">
            <h2>Highly Qualified Team</h2>
        </div>
        <div class="row">
            <div class="col-md-6 service">
                <div class="row">
                    <div class="col-auto">
                        <div class="image">
                            <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-18-300x300.jpg" alt="">
                        </div>
                    </div>
                    <div class="col">
                        <h4>
                            Alex Blackfire
                        </h4>
                        <h5>
                            Co-Founder, CEO
                        </h5>
                        <p>
                            Proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut sit amet semper arcu. Proin eget ex convallis eu viverra lorem dapibus loremipsum nulla dolor amet a tellus at euismod lorem ipsum.
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 service">
                <div class="row">
                    <div class="col-auto">
                        <div class="image">
                            <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-06-300x300.jpg" alt="">
                        </div>
                    </div>
                    <div class="col">
                        <h4>
                            Jacob Remmington
                        </h4>
                        <h5>Co-Founder, Creative Director</h5>
                        <p>
                            Etiam mollis libero vitae pulvinar bibendum. Morbi convallis metus eros, semper pharetra massa efficitur auctor. Proin eget ex convallis. Eget ex convallis eu viverra lorem dapibus a tellus at euismod lorem ipsum.
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 service">
                <div class="row">
                    <div class="col-auto">
                        <div class="image">
                            <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-16-300x300.jpg" alt="">
                        </div>
                    </div>
                    <div class="col">
                        <h4>
                            Miriam Richmond
                        </h4>
                        <h5>Financial Director</h5>
                        <p>
                            Lorem convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut sit amet semper arcu. Proin eget ex convallis es at euismod lorem ipsum amet. Etiam mollis libero vitae pulvinar aretra massa efficitur auctor.
                        </p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 service">
                <div class="row">
                    <div class="col-auto">
                        <div class="image">
                            <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-01-300x300.jpg" alt="">
                        </div>
                    </div>
                    <div class="col">
                        <h4>
                            Leonardo Black
                        </h4>
                        <h5>Marketing Director</h5>
                        <p>
                            Proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut sit amet semper arcu. Proin eget ex convallis eu viverra lorem dapibus a tellus at euismod lorem ipsum.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">

            <swiper :options="swiperOption" class="slick-slider ">
                <swiper-slide class="slick-slide">
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-17-100x100.jpg" alt="">
                    </div>
                    <h5>Henry Richards</h5>
                    <p>Photographer</p>
                </div>
                </swiper-slide>

                <swiper-slide class="slick-slide">
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-02-100x100.jpg" alt="">
                    </div>
                    <h5>Anna Lee</h5>
                    <p>HTML & CSS</p>
                </div>
                </swiper-slide>

                <swiper-slide class="slick-slide">
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-06-100x100.jpg" alt="">
                    </div>
                    <h5>Nick White</h5>
                    <p>Accountant</p>
                </div>
                </swiper-slide>

                <swiper-slide class="slick-slide">
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-12-100x100.jpg" alt="">
                    </div>
                    <h5>James Brown</h5>
                    <p>Content Manager</p>
                </div>
                </swiper-slide>

                <swiper-slide class="slick-slide">
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-25-100x100.jpg" alt="">
                    </div>
                    <h5>Diana Redwood</h5>
                    <p>Designer</p>
                </div>
                </swiper-slide>

                <swiper-slide class="slick-slide">
                <div class="item">
                    <div class="image">
                        <img class="img-fluid" src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/t-01-100x100.jpg" alt="">
                    </div>
                    <h5>William Black</h5>
                    <p>Programmer</p>
                </div>
                </swiper-slide>
            </swiper>

        </div>
    </section>
</template>

<script>
export default {
    name: 'AppHometeam',
    data () {
        return {
        swiperOption: {
            loop: true,
            slidesPerView: 5,
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
                slidesPerView: 5,
                spaceBetween: 5,
            },
            },
        },
        }
    }

}
</script>

<style lang="scss">
    .team {
        padding: 65px 65px;
    }
    .team h2 {
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

    .team h2::after {
        content: '';
        height: 3px;
        background-color: rgb(225, 61, 58);
        width: 200px;
        position: absolute;
        bottom: -10px;
        left: calc(50% - 100px);
    }
    .team p {
        color: rgb(51, 53, 57);
        font-size: 20px;
        font-weight: 400;
        line-height: 32px;
        text-align: center;
        max-width: 750px;
        margin-bottom: 80px;
    }

    .team .service {
        margin-bottom: 50px;
    }

    .team .service .image {
        width: 200px;
        height: 200px;
        border-radius: 50%;
        overflow: hidden;
        position: relative;
    }
    .team .service .image:after {
        content: '';
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(225, 61, 58, 0.36);
        opacity: 0;
        position: absolute;
        transition: all 0.3s linear;
    }
    .team .service .image:hover::after {
        opacity: 1;
    }
    .team .service .image img {
        max-width: 100%;
    }
    .team .service h2 {
        color: rgb(51, 53, 57);
        font-size: 20px;
        font-weight: 700;
        line-height: 30px;
        margin-bottom: 10px;
    }
    .team .service p {
        color: rgb(120, 125, 133);
        font-size: 15px;
        font-weight: 400;
        line-height: 26px;
        margin-bottom: 20px;
        text-align: left;
    }
    .team .service .btn {
        background-color: #e13d3a;
        border-radius: 3px;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: rgb(255, 255, 255);
        font-size: 13px;
        padding-bottom: 7px;
        padding-left: 14px;
        padding-right: 14px;
        padding-top: 8px;
        border: none;
    }
    .team .slick-slider {
        background-color: #f7f7f8;
    }
    .team .slick-slide .item {
        padding: 15px;
        text-align: center;
    }
    .team .slick-slide .item .image {
        position: relative;
        border-radius: 50%;
        width: 100px;
        height: 100px;
        overflow: hidden;
        margin: 0 auto;
        margin-bottom: 15px;
    }
    .team .slick-slide .item .image:after {
        content: '';
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(225, 61, 58, 0.36);
        opacity: 0;
        position: absolute;
        transition: all 0.3s linear;
    }
    .team .slick-slide .item h5 {
        color: rgb(51, 53, 57);
        font-size: 16px;
        font-weight: 700;
        line-height: 26px;
        text-align: center;
    }
    .team .slick-slide .item p {
        color: rgb(51, 53, 57);
        font-size: 13px;
        font-weight: 400;
        line-height: 23px;
        text-align: center;
        margin-bottom: 0;
    }
    
    .team .slick-slide:hover .item .image:after {
        opacity: 1;
    }
    .team .slick-prev {
        left: 0;
    }
    .team .slick-next {
        right: 0;
    }
    .team .slick-prev, .team .slick-next {
        width: 40px;
        height: 40px;
        z-index: 2;
    }
    .team .slick-prev::before, .team .slick-next::before {
        font-family: 'slick';
        font-size: 24px;
        line-height: 1;
        opacity: 0.75;
        color: #a7afb3;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    @include md {
        .service .row {
            display: block;
        }
    }
</style>