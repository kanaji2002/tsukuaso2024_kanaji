<h1> <strong>中国</strong></h1>


<!-- <a href="/shikoku">四国</a>
<a href="/area/hokkaidou">北海道</a> -->

<!-- 画像をリンクとして押せるようにする -->

<style>
    .image-container {
      position: relative;
      display: inline-block; /* 画像のサイズに合わせて親要素のサイズが変わる */
    }
  
    img {
      width: 100%; /* 画像のサイズを変更する場合 */
      height: auto;
    }
  


    .custom-button-tottori {
      background: url('image/prefecture/tottori.svg');
      background-size: cover;
      width:420px;
      height: 230px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 38%; /* 画像の上からの位置 (全体の30%) */
      left: 80%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }


    .custom-button-simane {
      background: url('image/prefecture/simane.svg');
      background-size: cover;
      width: 500px;
      height: 350px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 49%; /* 画像の上からの位置 (全体の30%) */
      left: 48%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }



    .custom-button-okayama {
      background: url('image/prefecture/okayama.svg');
      background-size: cover;
      width: 320px;
      height: 270px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 55%; /* 画像の上からの位置 (全体の30%) */
      left: 83%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }



    .custom-button-hirosima {
      background: url('image/prefecture/hirosima.svg');
      background-size: cover;
      width: 390px;
      height: 360px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 68%; /* 画像の上からの位置 (全体の30%) */
      left: 52%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }


    .custom-button-yamaguti {
      background: url('image/prefecture/yamaguti.svg');
      background-size: cover;
      width: 430px;
      height: 330px;
      color: white;
      border: none;
      font-size: 16px;
      /* background: transparent; */
      position: absolute;
      top: 77%; /* 画像の上からの位置 (全体の30%) */
      left: 20%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }


    .h3dayo {
text-align: center;
display: flex;
justify-content: center;
font-weight: 500;
font-size: 25px;}
  </style>
  <p class="h3dayo"> 各県を案内します．興味のある<strong>県</strong>を選んでください．</p>
  <div class="image-container">
    <!-- 画像を表示 -->
    <!-- <img src="/path/to/your-image.jpg" alt="Sample Image" />
   -->

        <img src="/image/prefecture/tyuugoku_pre.jpg" alt="Japan Image" />

    <a href="/tottori" class="custom-button-tottori"></a>
    <a href="/simane" class="custom-button-simane"></a>
    <a href="/okayama" class="custom-button-okayama"></a>
    <a href="/hirosima" class="custom-button-hirosima"></a>
    <a href="/yamaguti" class="custom-button-yamaguti"></a>
    <!-- <a href="/kinnki" class="custom-button-kinnki"></a>
    <a href="/shikoku" class="custom-button-shikoku"></a>
    <a href="/tyuugoku" class="custom-button-tyuugoku"></a>
    <a href="/kyuusyuu" class="custom-button-kyuusyuu"></a>
    <a href="/okinawa" class="custom-button-okinawa"></a> -->



    <!-- ボタン1を配置 -->
    <!-- <button class="button1" on:click={() => alert('Button 1 clicked!')}>Button 1</button> -->
  
    <!-- ボタン2を配置 -->
    
  </div>
  

