<template>
  <section class="consult">
      <div class="overlay">

      </div>
      <svg class="start-seprator" xmlns="http://www.w3.org/2000/svg" version="1.1" fill="#ffffff" width="100%" height="100" viewBox="0 0 4 0.266661" preserveAspectRatio="none" style="height: 100px;"><polygon class="fil0" points="4,0 4,0.266661 -0,0.266661 "></polygon></svg>
      <div class="content">
        <div class="row m-0 justify-content-center">
            <div class="col">
                <h2>Free First Consultation</h2>
                <p class="lead">
                    Etiam mollis libero vitae pulvinar bibendum. Morbi convallis metus eros, semper pharetra massa efficitur auctor amet convallis!
                </p>
                <p class="description">
                    Mollis libero vitae pulvinar bibendum. Morbi convallis metus eros, semper pharetra massa efficitur auctor. Etiam sit amet convallis erat. Class aptent taciti sociosqu ad litora torquent per conubia! Maecenas gravida lacus nec dolor suscipit faucibus.
                </p>
            </div>
            <div class="col consult-container">
                <div class="row m-0">
                    <div class="col-12">
                                <input type="text" class="validate[required]" placeholder="Name *" name="name" value="" aria-required="true">
                    </div>
                    <div class="col-12">
                        <input type="text" placeholder="E-mail" name="email" value="" aria-required="false">
                    </div>
                    <div class="col-12">
                        <input type="text" class="validate[required,custom[phone]]" placeholder="Telephone *" name="telephone" value="" aria-required="true">
                    </div>
                    <div class="col-12">
                        <textarea placeholder="Message" name="message" rows="4" aria-required="false"></textarea>
                    </div>
                    <div class="col-12">
                        <a href="#" class="btn">Consult Me!</a>
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
    name: 'AppHomeConsult',
    data () {
        return {

        }
    }

}
</script>

<style lang="scss">
    .consult {
        background-size: cover;
        background-repeat: no-repeat;
        background-color: rgba(0, 0, 0, 0);
        background-image: url("https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/img-row-051.jpg");
        background-attachment: fixed;
        position: relative;
        padding: 200px 65px;
    }
    @include xs {
        .consult {
            padding: 200px 15px;
        }
    }
    .consult .content {
        border: 9px double rgba(255, 255, 255, 0.3);
        padding-bottom: 60px;
        padding-left: 25px;
        padding-right: 25px;
        padding-top: 60px;
        position: relative;
        z-index: 1;
        
    }
    @include xs {
        .consult .content {
            padding-left: 15px;
            padding-right: 15px;
            
        }
    }
    .consult .overlay {
        background-color: rgba(0, 0, 0, 0.65);
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        z-index: 0;
    }
    .consult .start-seprator {
        position: absolute;
        top: 0;
        transform: scale(-1);
        left: 0;
        right: 0;
        z-index: 1;

    }
    .consult .end-seprator {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: 1;

    }
    .consult h2 {
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

    .consult h2::after {
        content: '';
        height: 3px;
        background-color: rgb(225, 61, 58);
        width: 200px;
        position: absolute;
        bottom: -10px;
        left: 0;
    }
    .consult p.lead {
        color: rgb(255, 255, 255);
        font-size: 20px;
        font-weight: 400;
        line-height: 32px;
        margin-bottom: 25px;
        text-align: left;
    }
    .consult p.description {
        color: #fff;
        font-size: 15px;
        margin-bottom: 10px;
    }
    
    .consult .consult-container {
        padding: 0 !important;
        max-width: 330px;
    }
    .consult .btn {
        background-color: rgb(225, 61, 58);
        align-items: center;
        border-radius: 3px;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: rgb(255, 255, 255);
        margin-right: 10px;
        padding-bottom: 11px;
        padding-left: 18px;
        padding-right: 18px;
        padding-top: 12px;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease-out;
        border: none;
    }
    .consult input ,
    .consult textarea {
        background-color: rgb(252, 252, 252);
        border: none;
        box-shadow: none;
        color: rgb(120, 125, 133);
        font-size: 14px;
        line-height: 26px;
        margin-bottom: 10px;
        min-height: 38px;
        padding-bottom: 5px;
        padding-left: 15px;
        padding-right: 15px;
        padding-top: 5px;
        width: 100%;
    }
    .consult input:focus {
        border: none;
        box-shadow: none;
        outline: none;
    }
</style>