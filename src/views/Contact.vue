<template>
  <div class="contact">
    <div class="contact-main-img">
      <div class="j-head">contact</div>
    </div>

    <div class="contact-contents1 mw1440 padding-tb-50">
      <div class="group">
        <div class="con-box">
          <v-icon>mdi-phone</v-icon>
          <div class="text-box">
            <p class="j-title">phone</p>
            <div class="j-text">010-0000-0000</div>
          </div>
        </div>

        <div class="con-box">
          <v-icon>mdi-map-marker</v-icon>
          <div class="text-box">
            <p class="j-title">address</p>
            <div class="j-text">경기도 시흥시 서울대학로</div>
          </div>
        </div>

        <div class="con-box">
          <v-icon>mdi-email</v-icon>
          <div class="text-box">
            <p class="j-title">email</p>
            <div class="j-text">jollybeen@gmail.com</div>
          </div>
        </div>
      </div>
    </div>

    <div class="contact-contents2 mw1440 padding-tb-50">
      <div class="group">
        <div class="img-box">
          <img src="../assets/contact/contact-img.jpg" alt="">
        </div>
        <div class="text-box fs16">
          <input type="text" placeholder="Name">
          <input type="text" placeholder="E-mail">
          <input type="text" placeholder="subject">
          <textarea rows="10" placeholder="Message"></textarea>
          <div class="btn-box">
            <button>send</button>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>



<style lang="scss" scoped>
  .contact-main-img{
    background-image: url(../assets/contact/main-img.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: bottom;
    height: 50vh;
    margin-bottom: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    .j-head{
      letter-spacing: 2px;
      font-weight: bold;
    }
  }

  .contact-contents1{
    .group{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .con-box{
      width: 33.33333%;
      padding: 0 20px;
      text-align: center;
      .v-icon{
        color: #5EE0A5;
        margin-bottom: 20px;
        font-size: 30px;
      }
      .j-title{ margin-bottom: 10px; color: #5EE0A5; font-weight: bold; }
    }
    .con-box:nth-child(2) {
      border-left: 1px solid #bebebe;
      border-right: 1px solid #bebebe;
    }
  }

  .contact-contents2{
    .group{ display: flex; }
    .img-box{
      width: 50%;
      img{
        width: 60%;
        margin: 0 auto;
      }
    }
    .text-box{
      width: 50%;
      input, textarea{
        background-color: #eee;
        width: 100%;
        padding: 10px 20px;
        margin-bottom: 20px;
      }
      input:focus, textarea:focus{
        outline: none;
        box-shadow: 0 0 0 2.5px rgba(119, 119, 119, .25);
      }
      .btn-box{ margin-top: 20px; text-align: center; }
      button{
        background-color: #3EDA93;
        color: #fff;
        padding: 10px 20px;
      }
    }
  }


  @media (max-width: 768px) {
    .contact-main-img{ margin-bottom: 30px; }
    .contact-contents1{ margin-bottom: 10px; }
    .contact-contents2{
      margin-bottom: 30px;
      .img-box{
        img{ width: 80%; }
      }
      .text-box{
        .btn-box{ margin-top: 0; }
      }
    }
  }

  @media (max-width: 650px) {
    .contact-contents2{
      .group{ flex-direction: column; }
      .img-box{
        margin: 0 auto 30px;
        img{ width: 100%; }
      }
      .text-box{
        width: 80%;
        margin: 0 auto;
      }
    }
  }

  @media (max-width: 500px) {
    .contact-contents1{
      .group{
        flex-direction: column;
      }
      .con-box{
        min-width: 240px;
        margin: 0 auto 20px;
        display: flex;
        .text-box{
          text-align: left;
        }
        .v-icon{
          margin-right: 20px;
          margin-bottom: auto;
        }
        .j-title{
        }
      }
      .con-box:nth-child(2) {
        border: none;
      }
    }
  }
  
</style>