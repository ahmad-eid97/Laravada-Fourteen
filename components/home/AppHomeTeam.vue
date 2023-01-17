<template>
  <section class="team">
    <div class="row justify-content-center">
      <h2>Highly Qualified Team</h2>
    </div>
    <div class="row justify-content-center">
      <div class="col-md-6 service" v-for="member in teams" :key="member.id">
        <div class="row">
          <div class="col-auto">
            <div class="image">
              <img :src="member.image" :alt="member.title" />
            </div>
          </div>
          <div class="col">
            <h4>
              {{ member.name }}
            </h4>
            <h5>
              {{ member.job }}
            </h5>
            <p>
              {{ member.description.substring(0, 200) }}
              {{ member.description.length > 200 ? "..." : "" }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-content-center">
      <swiper
        :options="swiperOption"
        class="slick-slider justify-content-center"
      >
        <swiper-slide
          class="slick-slide"
          v-for="member in teams"
          :key="member.id"
        >
          <div class="item">
            <div class="image">
              <img class="img-fluid" :src="member.image" :alt="member.title" />
            </div>
            <h5>
              {{ member.name }}
            </h5>
            <p>{{ member.job }}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHometeam",
  props: ["teams"],
  data() {
    return {
      swiperOption: {
        // loop: true,
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
    };
  },
};
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
.swiper-wrapper {
  justify-content: center !important;
}

.team h2::after {
  content: "";
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
  content: "";
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
  content: "";
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
.team .slick-prev,
.team .slick-next {
  width: 40px;
  height: 40px;
  z-index: 2;
}
.team .slick-prev::before,
.team .slick-next::before {
  font-family: "slick";
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
