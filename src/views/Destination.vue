<template>
  <div class="destination">
    <div class="destination-main-img">
      <div class="j-head">Popular destinations</div>
    </div>

    <div class="destination-photo-view mw1440 padding-tb-50">
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
    location :[
      { name: "busan", image: require("../assets/photo-view-busan.jpg") } ,
      { name: "danang", image: require("../assets/photo-view-danang.jpg") } ,
      { name: "hongkong", image: require("../assets/photo-view-hongkong.jpg") } ,
      { name: "singapore", image: require("../assets/photo-view-singapore.jpg") } ,
      { name: "thailand", image: require("../assets/photo-view-thailand.jpg") } ,
      { name: "bali", image: require("../assets/photo-view-bali.jpg") } ,
      { name: "boracay", image: require("../assets/photo-view-boracay.jpg") } ,
      { name: "cebu", image: require("../assets/photo-view-cebu.jpg") } ,
      { name: "hawaii", image: require("../assets/photo-view-hawaii.jpg") } ,
      { name: "phuket", image: require("../assets/photo-view-phuket.jpg") } ,
      { name: "las vegas", image: require("../assets/photo-view-las vegas.jpg") } ,
      { name: "san francisco", image: require("../assets/photo-view-sanfrancisco.jpg") } ,
      { name: "london", image: require("../assets/photo-view-london.jpg") } ,
      { name: "prague", image: require("../assets/photo-view-prague.jpg") } ,
      { name: "dubai", image: require("../assets/photo-view-dubai.jpg") },
      { name: "nha trang", image: require("../assets/photo-view-nhatrang.jpg") },
      { name: "taipei", image: require("../assets/photo-view-taipei.jpg") },
      { name: "seattle", image: require("../assets/photo-view-seattle.jpg") },
      { name: "sydney", image: require("../assets/photo-view-sydney.jpg") },
      { name: "rome", image: require("../assets/photo-view-rome.jpg") }
    ]
  })
}
</script>


<style lang="scss" scoped>
  .destination-main-img{
    background-image: url(../assets/destination/main-img.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    height: 50vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    .j-head{
      max-width: 80%;
      letter-spacing: 2px;
      font-weight: bold;
      word-break: normal;
      text-align: center;
    }
  }

  .destination-photo-view{
    max-width: 1240px;
    margin-top: 50px;
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
      img{ margin: 0; border-radius: 10px; }
      .j-title{
        background-color: rgba(0, 0, 0, .3);
        color: #fff;
        width: calc(100% - 40px);
        height: calc(100% - 40px);
        border-radius: 10px;
        padding: 20px;
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: 'Roboto Slab', serif;
        position: absolute;
        top: 20px;
      }
    }
  }



  @media (max-width: 768px) {
    .destination-photo-view{
      .photo-view-box{ width: 25%; }
    }
  }


  @media (max-width: 650px) {
    .destination-photo-view{
      .photo-view-box{ width: 33.33333%; }
    }
  }


  @media (max-width: 500px) {
    .destination-photo-view{
      .group{ margin: -10px; }
      .photo-view-box{
        width: 50%;
        padding: 10px;
        .j-title{
          width: calc(100% - 20px);
          height: calc(100% - 20px);
          top: 10px;
        }
      }
    }
  }
</style>