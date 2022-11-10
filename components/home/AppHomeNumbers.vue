<template>
  <section class="numbers">
      <div class="overlay">

      </div>
      <svg class="start-seprator" xmlns="http://www.w3.org/2000/svg" version="1.1" fill="#ffffff" width="100%" height="100" viewBox="0 0 4 0.266661" preserveAspectRatio="none" style="height: 100px;"><polygon class="fil0" points="4,0 4,0.266661 -0,0.266661 "></polygon></svg>
      <div class="content">
        <div class="row m-0 justify-content-center">
            <div class="col">
                <h2>Seven Business Company</h2>
                <p class="lead">
                    Lorem ipsum dolor amet volutpat. Nunc ut – for dictum purus lorem vel ante ac purus sollicitudin dictum ipsum eget ex convallis.
                </p>
                <p class="description">
                    Etiam mollis libero vitae pulvinar bibendum. Morbi convallis metus eros, semper pharetra massa efficitur auctor. Etiam sit amet convallis erat. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. In vel varius esteu gravidmi.
                </p>
                <p class="description">
                    Lorem ipsum dolor amet volutpat. Nunc ut – for dictum purus lorem vel ante ac purus sollicitudin dictum ipsum eget ex convallis.
                </p>
            </div>
            <div class="col-auto numbers-container">
                <div class="row m-0">
                    <div class="col-12 number">
                        <div class="row m-0">
                            <div class="col-auto icon">
                                <font-awesome-icon icon="fa-solid fa-clipboard-user" />
                            </div>
                            <div class="col">
                                <h3>
                                    16
                                </h3>
                                <h4>
                                    Specialists
                                </h4>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 number">
                        <div class="row m-0">
                            <div class="col-auto icon">
                                <font-awesome-icon icon="fa-solid fa-briefcase" />
                            </div>
                            <div class="col">
                                <h3>
                                    50+
                                </h3>
                                <h4>
                                    Projects Delivered
                                </h4>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 number">
                        <div class="row m-0">
                            <div class="col-auto icon">
                                <font-awesome-icon icon="fa-solid fa-star" />
                            </div>
                            <div class="col">
                                <h3>
                                    10+
                                </h3>
                                <h4>
                                    Industry Awards
                                </h4>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
      </div>
      <svg class="end-seprator" xmlns="http://www.w3.org/2000/svg" version="1.1" fill="#ffffff" width="100%" height="100" viewBox="0 0 4 0.266661" preserveAspectRatio="none" style="height: 100px;"><polygon class="fil0" points="4,0 4,0.266661 -0,0.266661 "></polygon></svg>
  </section>
</template>

<script>
export default {
    name: 'AppHomenumbers',
    data () {
        return {

        }
    }

}
</script>

<style lang="scss">
    .numbers {
        background-size: cover;
        background-repeat: no-repeat;
        background-color: rgba(0, 0, 0, 0);
        background-image: url("https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/img-row-053.jpg");
        background-attachment: fixed;
        position: relative;
        padding: 200px 65px;
    }
    @include xs {
        .numbers {
            padding: 200px 15px;
        }
    }
    .numbers .content {
        border: 9px double rgba(255, 255, 255, 0.3);
        padding-bottom: 10px;
        padding-left: 25px;
        padding-right: 25px;
        padding-top: 60px;
        position: relative;
        z-index: 1;
        
    }
    .numbers .overlay {
        background-color: rgba(0, 0, 0, 0.4);
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        z-index: 0;
    }
    .numbers .start-seprator {
        position: absolute;
        top: 0;
        transform: scale(-1);
        left: 0;
        right: 0;
        z-index: 1;

    }
    .numbers .end-seprator {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: 1;

    }
    .numbers h2 {
        clear: both;
        color: #fff;
        font-size: 34px;
        font-weight: 700;
        line-height: 44px;
        margin-bottom: 15px;
        position: relative;
        margin-bottom: 40px;
        text-align: left;
        padding: 0;
    }

    .numbers h2::after {
        content: '';
        height: 3px;
        background-color: rgb(225, 61, 58);
        width: 200px;
        position: absolute;
        bottom: -10px;
        left: 0;
    }
    .numbers p.lead {
        color: rgb(255, 255, 255);
        font-size: 20px;
        font-weight: 400;
        line-height: 32px;
        margin-bottom: 25px;
        text-align: left;
    }
    .numbers p.description {
        color: #fff;
        font-size: 15px;
        margin-bottom: 10px;
    }
    .numbers .number {
        width: 330px;
        padding-bottom: 45px;
    }
    .numbers .numbers-container {
        width: 330px;
    }
    .numbers .number .icon {
        background-clip: border-box;
        background-color: rgb(225, 61, 58);
        border-radius: 50%;
        color: rgb(255, 255, 255);
        height: 44px;
        line-height: 44px;
        width: 44px;
        padding: 0;
        font-size: 24px;
        text-align: center;
    }
    .numbers .number h3 {
        color: rgb(255, 255, 255);
        font-size: 40px;
        font-weight: 700;
        line-height: 50px;
        text-align: left;
    }
    .numbers .number h4 {
        color: rgb(255, 255, 255);
        font-size: 20px;
        line-height: 30px;
        text-align: left;
    }
</style>