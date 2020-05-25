<template>
  <div class="home">
    <div class="main-img"></div>

    <div class="home-find">
      <div class="find-group radius-5 fs14">
        <div class="find-box">
          <v-icon class="color-green">mdi-map-marker</v-icon>
          <v-text-field label="Location"></v-text-field>
        </div>
        <div class="find-box date-box">
          <v-icon class="color-green">mdi-calendar</v-icon>
          <v-text-field label="Date"></v-text-field>
        </div>
        <!-- <div class="find-box">
          <v-icon class="color-green">mdi-map-marker</v-icon>
          <v-text-field label="Location"></v-text-field>
        </div> -->
        <button class="uppercase bg-green">search</button>
      </div>
    </div>

    <div class="home-text mw1440 padding-tb-50">
      <div class="padding-tb-50">
        <p class="j-title">Lorem Ipsum is simply dummy text of the printing and typesetting industry.</p>
        <p class="j-text">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      </div>
    </div>

    <div class="home-card-view mw1440 padding-tb-50">
      <div class="group">
        <div class="card-view-box" v-for="cardView in cardViewBox" :key="cardView">
          <img :src="cardView.image" alt="">
          <div class="text-box">
            <div class="title-box">
              <p class="j-title">{{cardView.title}}</p>
              <p class="j-text">{{cardView.price}}</p>
            </div>
            <p class="j-text">{{cardView.text}}</p>
          </div>
        </div>
      </div>
    </div>

    <div class="home-img-text">
      <div class="text-box">
        <p class="j-head">sample</p>
        <p class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      </div>
    </div>

    <div class="home-photo-view mw1440 padding-tb-50">
      <div class="group">
        <div class="photo-view-box" v-for="city in location" :key="city">
          <img :src="city.image" alt="">
          <p class="j-title">{{city.name}}</p>
        </div>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  data: () => ({
    cardViewBox: [
      { title: "sample", price: "$100", text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.", image: require("../assets/home/card-view01.jpg") },
      { title: "sample", price: "$360", text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.", image: require("../assets/home/card-view02.jpg") },
      { title: "sample", price: "$240", text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.", image: require("../assets/home/card-view03.jpg") },
      { title: "sample", price: "$500", text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry.", image: require("../assets/home/card-view01.jpg") }
    ],
    location :[
      { name: "busan", image: require("../assets/home/photo-view-busan.jpg") } ,
      { name: "danang", image: require("../assets/home/photo-view-danang.jpg") } ,
      { name: "hongkong", image: require("../assets/home/photo-view-hongkong.jpg") } ,
      { name: "singapore", image: require("../assets/home/photo-view-singapore.jpg") } ,
      { name: "thailand", image: require("../assets/home/photo-view-thailand.jpg") } ,
      { name: "bali", image: require("../assets/home/photo-view-bali.jpg") } ,
      { name: "boracay", image: require("../assets/home/photo-view-boracay.jpg") } ,
      { name: "cebu", image: require("../assets/home/photo-view-cebu.jpg") } ,
      { name: "hawaii", image: require("../assets/home/photo-view-hawaii.jpg") } ,
      { name: "phuket", image: require("../assets/home/photo-view-phuket.jpg") } ,
      { name: "las vegas", image: require("../assets/home/photo-view-las vegas.jpg") } ,
      { name: "san francisco", image: require("../assets/home/photo-view-sanfrancisco.jpg") } ,
      { name: "london", image: require("../assets/home/photo-view-london.jpg") } ,
      { name: "prague", image: require("../assets/home/photo-view-prague.jpg") } ,
      { name: "dubai", image: require("../assets/home/photo-view-dubai.jpg") }
    ]
  })



  // name: 'Home',
  // components: {
  //   HelloWorld
  // }
}
</script>



<style lang="scss" scoped>
  .main-img{
    background-image: url(../assets/home/main-img.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 80vh;
  }

  .home-find{
    padding: 0 40px 50px;
    .find-group{
      background-color: #fff;
      box-shadow: 0 2px 10px -5px #bebebe;
      max-width: 1080px;
      margin: -55px auto 0;
      padding: 20px 0;
      display: flex;
      align-items: center;
    }
    .find-box{
      padding: 0 20px;
      display: flex;
      align-items: center;
      position: relative;
      .v-icon{
        color: #3EDA93;
        margin-right: 6px;
      }
      .v-input{ max-width: 200px; }
    }
    .find-box:nth-child(1)::before{
      content: "";
      width: 1px;
      height: 30px;
      background: #bebebe;
      position: absolute;
      right: 0;
    }
    button{
      margin: 20px 20px 20px auto;
      padding: 10px 20px;
      font-weight: bold;
    }
  }

  .home-text{
    text-align: center;
    .j-title{
      width: 50%;
      max-width: 700px;
      margin-left: auto;
      margin-right: auto;
      text-transform: none;
      line-height: 1.5;
    }
    .j-text{
      width: 80%;
      max-width: 1000px;
      margin: 0 auto;
    }
  }

  .home-card-view{
    .group{
      margin: -20px;
      display: flex;
      flex-wrap: wrap;
    }
    .card-view-box{
      padding: 20px;
      width: 25%;
    }
    .title-box{
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;

      .j-title{ margin: 0; }
      .j-text{ color: #FF7037; font-weight: bold; }
    }
  }

  .home-img-text{
    background-image: url(../assets/home/img-text.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    margin: 50px 0;
    padding: 100px;
    display: flex;
    align-items: center;
    .text-box{
      background-color: #fff;
      max-width: 800px;
      margin: 0 auto;
      padding: 50px;
      text-align: center;
    }

  }

  .home-photo-view{
    max-width: 1240px;
    margin-bottom: 50px;
    .group{
      margin: -20px;
      display: flex;
      flex-wrap: wrap;
    }
    .photo-view-box{
      width: 20%;
      padding: 20px;
      position: relative;
      img{ margin: 0; width: 100%; height: 100%; }
      .j-title{
        background-color: rgba(0, 0, 0, .3);
        color: #fff;
        width: calc(100% - 40px);
        height: calc(100% - 40px);
        padding: 20px;
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: 'Roboto Slab', serif;
        word-break:break-all;
        position: absolute;
        top: 20px;
      }
    }
  }





  @media (max-width: 768px) {
    .main-img{ height: 50vh; }

    .home-find{
      padding: 30px;
      .find-group{
        margin-top: -130px;
      }
    }

    .home-card-view{
      .card-view-box{
        width: 50%;
      }
    }

    .home-photo-view{
      .photo-view-box{
        width: 33.33333%;
      }
    }
  }


  @media (max-width: 730px) {
    .home-find{
      .find-group{
        max-width: 80%;
        flex-direction: column;
      }
      .find-box{ padding: 0; }
      .find-box:nth-child(1)::before{ display: none; }
      button{ margin: 20px auto; }
    }
  }


  @media (max-width: 500px) {
    .home-find{
      padding: 20px;
      .find-group{ max-width: 90%; }
      button{ margin: 10px auto 0; }
    }

    .home-card-view{
      .group{ margin: -10px; }
      .card-view-box{ padding: 10px; }
    }
    

    .home-img-text{
      margin: 40px 0;
      padding: 80px 60px;
    }

    .home-photo-view{
      margin-bottom: 40px;
      .group{ margin: -10px; }
      .photo-view-box{
        width: 50%;
        padding: 10px;
        .j-title{
          width: calc(100% - 20px);
          height: calc(100% - 20px);
          top: 10px;
          font-size: 16px;
        }
      }
    }
  }

</style>


<style>
.theme--light.v-text-field > .v-input__control > .v-input__slot:before {
  border-color: #3EDA93;
}
.theme--light.v-text-field:not(.v-input--has-state):hover > .v-input__control > .v-input__slot:before{
  border-color: #3EDA93;
}
.v-text-field .v-label{ color: #bebebe; }
.theme--light.v-input{ color: #3EDA93; }
.v-text-field .v-label--active{
  color: #3EDA93;
  transform: translateX(-10px) translateY(-18px) scale(0.75);
}
</style>