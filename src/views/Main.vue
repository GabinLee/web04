<template>
  <div class="main-container">
    <header id="header">
      <div class="h-container mw1440">
        <div class="logo-box">
          <a href="/web04" class="font-roboto">SAMPLE</a>
        </div>
        <nav class="nav-box uppercase fs14">
          <router-link to="/" class="nav-item" :class="{ checked : selectedIndex == 0 ? true : false }" @click.native="clickedNavItem(0)" onclick="window.scrollTo(0,0);"> home </router-link>

          <router-link to="/destination" class="nav-item" :class="{ checked : selectedIndex == 1 ? true : false }" @click.native="clickedNavItem(1)" onclick="window.scrollTo(0,0);"> destination </router-link>

          <router-link to="/about" class="nav-item menu-item" :class="{ checked : selectedIndex == 2 ? true : false }" @click.native="clickedNavItem(2)" onclick="window.scrollTo(0,0);"> about </router-link>

          <router-link to="/contact" class="nav-item" :class="{ checked : selectedIndex == 3 ? true : false}" @click.native="clickedNavItem(3)" onclick="window.scrollTo(0,0);"> contact </router-link>

          <!-- <router-link to="/contact" class="nav-item" :class="{ checked : selectedIndex == 4 ? true : false }" @click.native="clickedNavItem(4)">
            <span>contact</span>
          </router-link> -->
        </nav>

        <div class="mobile-menu-btn">
          <button v-ripple @click="openMobileNav">
            <v-icon>mdi-menu</v-icon>
          </button>
        </div>
      </div>
    </header>

    <div id="mobile-nav-container" @click="closeMobileNav">
      <div id="mobile-nav-group" class="fs16 uppercase">  
        <button v-ripple @click="closeMobileNav">
          <v-icon>mdi-close</v-icon>
        </button>
        <div class="mobile-nav-box mobile-nav-box-home">
          <router-link to="/" class="nav-item">
            <p>home</p>
          </router-link>
        </div>

        <div class="mobile-nav-box">
          <router-link to="/destination" class="nav-item">
            <p>destination</p>
          </router-link>
        </div>
        
        <div class="mobile-nav-box">
          <router-link to="/about" class="nav-item">
            <p>about</p>
          </router-link>
        </div>

        <div class="mobile-nav-box">
          <router-link to="/contact" class="nav-item">
            <p>contact</p>
          </router-link>
        </div>
      </div>
    </div>

    <main>
      <router-view />
    </main>
    
    <footer>
      <div class="f-container mw1440">
        <div class="logo-font j-head">Jollybeen</div>
        <div class="info-box">
          <div class="j-text">사업자등록번호 : 000-00-00000</div> |
          <div class="j-text">주소 : 경기도 시흥시 서울대학로</div> |
          <div class="j-text">대표 : OOO</div> |
          <div class="j-text">TEL : 000-0000-0000</div>
        </div>
        <div class="social-box">
          <a href="" class="insta">
            <v-icon>mdi-instagram</v-icon>
          </a>
          <a href="">
            <v-icon>mdi-facebook</v-icon>
          </a>
        </div>
      </div>
    </footer>


    <!-- <div class="find-box radius-5 fs14">
      <button class="uppercase" style="background: #2c9bf1">search</button>
      <button class="uppercase" style="background: #00c772">search</button>
      <button class="uppercase" style="background: #ffd24d">search</button>
      <button class="uppercase" style="background: #ff4900">search</button>
      <button class="uppercase" style="background: #8c8cf7">search</button>
    </div> -->
  </div>
</template>


<script>
export default {
  data: () => ({
    selectedIndex: 0
  }),
  created() {
    // this.$router.push({
    //   path: '/home'
    // })
    window.onscroll = function () {
      if (document.body.scrollTop > 80 || document.documentElement.scrollTop > 80 ) {
        document.getElementById("header").classList.add('scroll-header')
      } else{
        document.getElementById("header").classList.remove('scroll-header')
      }
    }
    // window.onload = function() {
    //   setTimeout(function() {
    //     scrollTo(0,0);
    //   }, 100);
      
    // }
  },
  mounted() {
    var NavItems = document.getElementsByClassName('nav-item');
    console.log(NavItems);
    console.log(NavItems[0]);
    this.sum(1, 2);
    
  },
  methods: {
    sum(num1, num2) {
      console.log(num1 + num2);
    },
    clickedNavItem(index) {
      this.selectedIndex = index;
    },
    openMobileNav() {
      document.getElementById('mobile-nav-container').style.width = "100%"
      document.getElementById('mobile-nav-group').style.width = "300px"
    },
    closeMobileNav() {
      document.getElementById('mobile-nav-container').style.width = "0"
      document.getElementById('mobile-nav-group').style.width = "0"
    }
  }
}
</script>



<style lang="scss">
.main-container{
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}


/* header */
  header{
    width: 100%;
    height: 80px;
    // box-shadow: 0 1px 3px rgba(0, 0, 0, .2);
    position: fixed;
    z-index: 999;
    .logo-box{
      display: flex;
      align-items: center;
      a{ font-size: 40px; color: #fff; }
    }
    .nav-box{
      margin-right: -14px;
      .nav-item{
        height: 100%;
        line-height: 80px;
        margin-right: 20px;
        padding: 0 14px;
        color: #fff;
        font-weight: 600;
        position: relative;
        transition: all 0.3s ease;
      }
      .nav-item:last-child{ margin: 0; }
      .nav-item:hover, .checked{ color: #222; font-weight: bold; }
    }
    .menu-item{
      position: relative;
      .dropdown-group{
        background-color: #f7f7f7;
        height: 0px;
        border-bottom-left-radius: 5px;
        border-bottom-right-radius: 5px;
        box-shadow: 0 2px 3px rgba(0, 0, 0, .2);
        overflow: hidden;
        position: absolute;
        left: 0;
        transition: .5s;
        cursor: default;
        .dropdown-box{
          margin: 14px;
        }
        a{
          width: 100%;
          height: 40px;
          border-radius: 5px;
          padding: 0px 20px;
          transition: .2s;
          display: flex;
          align-items: center;
          justify-content: center;
        }
        a:last-child{ margin-bottom: 0; }
        a:hover{
          background-color: #1BB850;
          color: #fff;
        }
      }
    }
    .menu-item:hover .dropdown-group{ height: 230px; }
  }
  .h-container{
    height: 100%;
    display: flex;
    justify-content: space-between;
  }

  .scroll-header{
    background-color: #fff;
    transition-duration: .2s;
    box-shadow: 0 2px 2px 0 #eee;
    .logo-box{
      a{ color: #399AE3; }
    }
    .nav-box{
      .nav-item{ color: #222; }
      .nav-item:hover, .checked{ color: #399AE3; }
    }
    .mobile-menu-btn button .v-icon{
      color: #000;
    }
    
  }

  .mobile-menu-btn{
    margin-right: -10px;
    display: none;
    button{
      color: #3EDA93;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      margin: 20px 0;
      .v-icon{ color: #fff; }
    }
  }
  #mobile-nav-container{
    background-color: rgba(0, 0, 0, .8);
    width: 0;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    z-index: 999;
    cursor: pointer;
  }
  #mobile-nav-group{
    background-color: #fff;
    width: 0;
    height: 100%;
    margin-left: auto;
    display: flex;
    flex-direction: column;
    transition: .5s;
    overflow: hidden;
    button{
      color: #1bb850;
      width: 40px;
      height: 40px;
      margin: 20px 20px 20px auto;
      border-radius: 50%;
    }
    button:hover{ background-color: rgba(174, 240, 210, .5); }

    .mobile-nav-box{
      margin: 0 10px;
      border-bottom: 1px solid rgba(0, 0, 0, .2);
      padding: 10px;
    }
    .mobile-nav-box-home { border-top: 1px solid rgba(0, 0, 0, .2); }
    .nav-item{
      color: #1bb850;
      width: 100%;
      border-radius: 5px;
      padding: 14px 0;
      text-align: center;
      p{
        color: #000;
      }
    }
    .nav-item:hover{ background-color: rgba(174, 240, 210, .5); }
  }
  


/* main */
  main{
    overflow: hidden;
  }


/* footer */
  footer{
    background-color: #999;
    margin-top: auto;
    text-align: center;
    color: #fff;
    .f-container{ padding: 40px; }
    .logo-font{ text-transform: none; }
    .info-box{
      margin-bottom: 20px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      .j-text{
        padding: 0 20px;
      }
    }
    .social-box{
      .v-icon{ color: #fff; }
      .insta{ margin-right: 20px; }
    }
  }



/* 반응형 */
  @media (max-width: 1000px){
  }

  @media (max-width: 768px) {
    header{
      height: 60px;
      .logo-box{
        a{ font-size: 32px; }
      }
      .nav-box{ display: none; }
    }
    .mobile-menu-btn{
      display: block;
      button{
        margin: 10px 0;
      }
    }

    footer{
      .f-container{ padding: 30px; }
    }
  }

  @media (max-width: 600px) {
    header{
      .logo-box{
        a{ font-size: 26px; }
      }
    }
    #mobile-nav-group{
      button{
        margin: 20px 10px 20px auto;
      }
    }

    footer{
      .f-container{ padding: 20px; }
    }
  }
</style>
