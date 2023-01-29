<template>
  <section class="contact">
    <div class="overlay"></div>
    <svg
      class="start-seprator"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      fill="#ffffff"
      width="100%"
      height="100"
      viewBox="0 0 4 0.266661"
      preserveAspectRatio="none"
      style="height: 100px"
    >
      <polygon class="fil0" points="4,0 4,0.266661 -0,0.266661 "></polygon>
    </svg>
    <div class="content">
      <div class="row m-0 justify-content-center box">
        <div class="col-4 contact-info">
          <h2>Get In Touch!</h2>
          <p class="lead">
            {{
              $store.state.websiteSettings.find(
                (one) => one.key === "description"
              ).plain_value
            }}
          </p>
        </div>
        <div class="col contact-container">
          <div class="row m-0">
            <div class="col-6 item">
              <div class="icon">
                <font-awesome-icon icon="fa-solid fa-location-dot" />
              </div>
              <h3>Address</h3>
              <p>
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "contact_address"
                  ).plain_value
                }}
              </p>
            </div>
            <div class="col-6 item">
              <div class="icon">
                <font-awesome-icon icon="fa-solid fa-phone" />
              </div>
              <h3>Phone</h3>
              <p style="font-size: 20px">
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "contact_phone"
                  ).plain_value
                }}
              </p>
            </div>
            <div class="col-6 item">
              <div class="icon">
                <font-awesome-icon icon="fa-solid fa-clock" />
              </div>
              <h3>Business Hours</h3>
              <p>
                Mon – Fri …… 10 am – 8 pm
                <br />
                Sat, Sun …… Closed
              </p>
            </div>
            <div class="col-6 item">
              <div class="icon">
                <font-awesome-icon icon="fa-solid fa-envelope" />
              </div>
              <h3>Email</h3>
              <p>
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "email"
                  ).plain_value
                }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeContact",
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.contact {
  background-size: cover;
  background-repeat: no-repeat;
  background-color: rgba(0, 0, 0, 0);
  background-image: url("https://the7.io/business-one-page/wp-content/uploads/sites/36/2016/12/img-row-052.jpg");
  background-attachment: fixed;
  position: relative;
  padding: 200px 65px 65px;
}
@include xs {
  .contact {
    padding: 200px 15px 55px;
  }
}
.contact .content {
  border: 9px double rgba(255, 255, 255, 0.3);
  padding-bottom: 60px;
  padding-left: 25px;
  padding-right: 25px;
  padding-top: 60px;
  position: relative;
  z-index: 1;
}
@include xs {
  .contact .content {
    padding-left: 5px;
    padding-right: 5px;
  }
}
@include sm {
  .box {
    display: block;
  }
}
.contact .overlay {
  background-color: rgba(0, 0, 0, 0.65);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 0;
}
.contact .start-seprator {
  position: absolute;
  top: 0;
  transform: scale(-1);
  left: 0;
  right: 0;
  z-index: 1;
}
.contact .end-seprator {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 1;
}
.contact h2 {
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

.contact h2::after {
  content: "";
  height: 3px;
  background-color: rgb(225, 61, 58);
  width: 200px;
  position: absolute;
  bottom: -10px;
  left: 0;
}
.contact p.lead {
  color: rgb(255, 255, 255);
  font-size: 20px;
  font-weight: 400;
  line-height: 32px;
  margin-bottom: 25px;
  text-align: left;
}
.contact p.description {
  color: #fff;
  font-size: 15px;
  margin-bottom: 10px;
}

.contact .contact-container {
  width: 330px;
}
.contact .item {
  margin-bottom: 45px;
}
.contact .item .icon {
  background-clip: border-box;
  background-color: rgb(225, 61, 58);
  border-radius: 50%;
  color: rgb(255, 255, 255);
  height: 36px;
  line-height: 38px;
  width: 36px;
  padding: 0;
  font-size: 20px;
  text-align: center;
  margin: 0 auto;
}
.contact .item h3 {
  color: rgb(255, 255, 255);
  font-size: 14px;
  line-height: 14px;
  margin-bottom: 15px;
  margin-top: 25px;
  text-align: center;
}
.contact .item p {
  color: rgb(255, 255, 255);
  font-size: 15px;
  text-align: center;
}
@include sm {
  .contact-info {
    width: unset !important;
  }
  .content .contact-container {
    width: unset !important;
  }
}
</style>
