<template>
  <div id="app">
    <router-view/>
  </div>
</template>



<style lang="scss">
/* default setting */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
    word-break: break-all;
    // font-family: 'Montserrat', 'Nanum Gothic';
  }
  ::selection{ background-color: rgba(62, 218, 147, .3); color: inherit; }
  html, body{ font-size: 10px; }

  a{ display: inline-block; text-decoration: none; color: inherit; }
  button{ background-color: transparent; border: none; border-radius: 5px; cursor: pointer; }
  button:focus{ outline: none; }

  img{ width: 100%; margin-bottom: 30px; display: block; }

  .mw1440{ max-width: 1440px; margin: 0 auto; padding-left: 40px; padding-right: 40px; }
  .padding-50{ padding: 50px; }
  .padding-tb-50{ padding-top: 50px; padding-bottom: 50px; }
  .radius-5{ border-radius: 5px; }


  .logo-font{ font-family: 'Delius Swash Caps', cursive; }
  .font-roboto{ font-family: 'Roboto Slab', serif; }
  .mj-font{ font-family: 'Nanum Myeongjo'; }
  .uppercase{ text-transform: uppercase; }
  .bg-red{ background-color: #FFB599; color: #fff; }
  .bg-yellow{ background-color: #FFD399; color: #fff; }
  .bg-green{ background-color: #3eda93; color: #fff; }
  .bg-blue{ background-color: #399AE3; color: #fff; }
  .bg-purple{ background-color: #C2C3FA; color: #fff; }
    

  .j-main-head{
    font-size: 80px;
    letter-spacing: 10px;
  }
  .j-head{
    font-size: 36px;
    margin-bottom: 30px;
    text-transform: uppercase;
  }
  .j-title{
    font-size: 20px;
    margin-bottom: 20px;
    text-transform: uppercase;  
  }
  .j-text{ font-size: 16px; line-height: 1.5; }
  .fs24{ font-size: 24px; }
  .fs16{ font-size: 16px; }
  .fs14{ font-size: 14px; }


/* 반응형 */
  @media (max-width: 1000px){
    .padding-50{ padding: 40px; }
    .padding-tb-50{ padding-top: 40px; padding-bottom: 40px; }
  }


  @media (max-width: 768px) {
    .mw1440{ padding-left: 30px; padding-right: 30px; }
    .padding-50{ padding: 30px; }
    .padding-tb-50{ padding-top: 30px; padding-bottom: 30px; }
    img{ margin-bottom: 20px; }

    .j-head{
      font-size: 30px;
      margin-bottom: 26px;
    }
    .j-title{
      font-size: 16px;
      margin-bottom: 16px;
    }
    .j-text{ font-size: 14px; }
    .fs24{ font-size: 20px; }
    .fs16{ font-size: 14px; }
    .fs14{ font-size: 12px; }
  }


  @media (max-width: 600px) {
    .mw1440{ padding-left: 20px; padding-right: 20px; }
    .padding-50{ padding: 20px; }
    .padding-tb-50{ padding-top: 20px; padding-bottom: 20px; }    

    .j-head{
      font-size: 26px;
      margin-bottom: 20px;
    }
    .j-title{
      font-size: 14px;
      margin-bottom: 14px;
    }
    .j-text{ font-size: 12px; }
    .fs24{ font-size: 16px; }
    .fs16{ font-size: 12px; }
    .fs14{ font-size: 10px; }
  }


</style>
