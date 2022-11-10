<template>
  <section class="services">
      <div class="row justify-content-center">
          <h2>Seven Business Company</h2>
          <p>
              Whatever the mind of man can conceive and believe, it can achieve. Thoughts are things! And powerful things at that, when mixed with definiteness of purpose, and burning desire, can be translated into riches.
          </p>
      </div>
      <div class="row">
          <div class="col-md-6 service">
              <div class="row">
                  <div class="col-auto">
                      <div class="image">
                          <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/b-009-300x300.jpg" alt="">
                      </div>
                  </div>
                  <div class="col">
                      <h4>
                        Proin eget ex convallis
                      </h4>
                      <p>
                          Ut sit amet semper arcu – dolor proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod. Morbi tellus at euismod lorem ipsum dolor.
                      </p>
                      <a href="#" class="btn">View Details</a>
                  </div>
              </div>
          </div>
          <div class="col-md-6 service">
              <div class="row">
                  <div class="col-auto">
                      <div class="image">
                          <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/b-001-300x300.jpg" alt="">
                      </div>
                  </div>
                  <div class="col">
                      <h4>
                        Viverra lorem pretium
                      </h4>
                      <p>
                          Ut sit amet semper arcu. Proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut sit amet semper arcu.
                      </p>
                      <a href="#" class="btn">View Details</a>
                  </div>
              </div>
          </div>
          <div class="col-md-6 service">
              <div class="row">
                  <div class="col-auto">
                      <div class="image">
                          <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/b-005-300x300.jpg" alt="">
                      </div>
                  </div>
                  <div class="col">
                      <h4>
                        Morbi tellus at euismod
                      </h4>
                      <p>
                          Proin eget ex convallis eu viverra lorem pretium. Morbi dapibus a tellus at euismod. Ut sit amet semper arcu. Proin eget ex convallis eu viverra lorem dapibus a tellus at euismod.
                      </p>
                      <a href="#" class="btn">View Details</a>
                  </div>
              </div>
          </div>
          <div class="col-md-6 service">
              <div class="row">
                  <div class="col-auto">
                      <div class="image">
                          <img src="https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/b-008-300x300.jpg" alt="">
                      </div>
                  </div>
                  <div class="col">
                      <h4>
                        Eget malesuada dolor
                      </h4>
                      <p>
                          Tristique eget malesuada sed, viverra at sapien. Maecenas gravida lacus nec dolor apibus a tellus at euismod. Ut sit amet semper arcu. Proin eget ex convallis eu viverra
                      </p>
                      <a href="#" class="btn">View Details</a>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeServices',
    data () {
        return {

        }
    }

}
</script>

<style lang="scss">
    .services {
        padding: 65px 65px 15px;
    }
    @include xs {
        .services {
            padding: 65px 25px 15px;
        }
    }
    .services h2 {
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

    .services h2::after {
        content: '';
        height: 3px;
        background-color: rgb(225, 61, 58);
        width: 200px;
        position: absolute;
        bottom: -10px;
        left: calc(50% - 100px);
    }
    .services p {
        color: rgb(51, 53, 57);
        font-size: 20px;
        font-weight: 400;
        line-height: 32px;
        text-align: center;
        max-width: 750px;
        margin-bottom: 80px;
    }

    .services .service {
        margin-bottom: 50px;
    }

    .services .service .image {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        overflow: hidden;
        position: relative;
    }
    .services .service .image:after {
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
    .services .service .image:hover::after {
        opacity: 1;
    }
    .services .service .image img {
        max-width: 100%;
    }
    .services .service h2 {
        color: rgb(51, 53, 57);
        font-size: 20px;
        font-weight: 700;
        line-height: 30px;
        margin-bottom: 10px;
    }
    .services .service p {
        color: rgb(120, 125, 133);
        font-size: 15px;
        font-weight: 400;
        line-height: 26px;
        margin-bottom: 20px;
        text-align: left;
    }
    .services .service .btn {
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
    @include xs {
        .service {
            .row {
                display: block;
            }
        }
    }
</style>