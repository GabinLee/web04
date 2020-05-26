<template>
  <div class="about">
    <div class="about-main-img">
      <div class="j-head">about</div>
    </div>

    <div class="about-intro mw1440 padding-tb-50">
      <div class="group">
        <div class="img-box padding-50">
          <img src="../assets/about/intro.jpg" alt="">
        </div>
        <div class="text-box padding-50">
          <p class="j-title fs24 font-roboto">sample</p>
          <p class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
        </div>
      </div>
    </div>

    <div class="about-contents1">
      <div class="group mw1440 padding-50">
        <p class="j-head">sample</p>
        <p class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
        <div class="img-group">
          <div class="img-box padding-50">
            <div class="img-frame">
              <img src="../assets/about/01.jpg" alt="">
            </div>
          </div>
           <div class="img-box padding-50">
            <div class="img-frame">
              <img src="../assets/about/02.jpg" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="about-contents2 mw1440 padding-tb-50">
      <div class="person-box">
        <div class="img-box padding-tb-50">
          <img src="../assets/about/03.jpg" alt="">
        </div>
        <div class="text-box padding-tb-50">
          <p class="j-title">sample</p>
          <p class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
        </div>
      </div>
      <div class="person-box">
        <div class="text-box padding-tb-50">
          <p class="j-title">sample</p>
          <p class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
        </div>
        <div class="img-box padding-tb-50">
          <img src="../assets/about/04.jpg" alt="">
        </div>
      </div>
    </div>
  </div>
</template>



<style lang="scss" scoped>
  .about-main-img{
    background-image: url(../assets/about/main-img.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: bottom;    height: 50vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    .j-head{
      letter-spacing: 2px;
      font-weight: bold;
    }
  }

  .about-intro{
    .group{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .img-box{
      width: 40%;
      img{ margin-bottom: 0; border-radius: 50%; }
    }
    .text-box{
      width: 60%;
      display: flex;
      justify-content: center;
      flex-direction: column;
      text-align: center;
    }
  }

  .about-contents1{
    background-color: #DFF9ED;
    .group{ text-align: center; }
    .j-text{
      max-width: 900px;
      margin: 0 auto;
    }
    .img-group{
      display: flex;
      flex-wrap: wrap;
    }
    .img-box{ width: 50%; }
    .img-frame{
      background-color: #fff;
      padding: 20px;
      img{ margin: 0; }
    }
  }

  .about-contents2{
    .person-box{
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
    }
    .img-box{
      width: 30%;
      padding-left: 25px;
      padding-right: 25px;
      img{ margin-bottom: 0; }
    }
    .text-box{
      width: 70%;
      padding-left: 25px;
      padding-right: 25px;
    }
  }



  @media (max-width: 768px) {
    .about-intro{
      .img-box{ width: 45%; }
      .text-box{ width: 55%; }
    }

    .about-contents2{
      .img-box{ width: 40%; }
      .text-box{ width: 60%; }
    }
  }


  @media (max-width: 650px) {
    .about-contents2{
      .img-box{ width: 50%; }
      .text-box{ width: 50%; }
    }
  }


  @media (max-width: 500px) {
    .about-intro{
      .group{ flex-direction: column; }
      .img-box{
        width: 70%;
        margin: 0 auto;
      }
      .text-box{ width: 100%; }
    }

    .about-contents1{
      .img-group{ margin: 10px -10px -10px; }
      .img-box{ padding: 10px; }
      .img-frame{ padding: 10px; }
    }

    .about-contents2{
      .person-box{
        flex-direction: column;
      }
      .person-box:nth-child(2){ flex-direction: column-reverse; }

      .img-box{
        width: 70%;
        margin: 0 auto;
      }
      .text-box{
        width: 100%;
        margin-top: -20px;
        padding-left: 10px;
        padding-right: 10px;
        text-align: center;
      }
    }
  }
</style>