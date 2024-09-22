<!-- src/routes/index.svelte -->
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
  
    .button1 {
      position: absolute;
      top: 30%; /* 画像の上からの位置 (全体の30%) */
      left: 40%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }
  
    .button2 {
      position: absolute;
      top: 70%;
      left: 60%;
      transform: translate(-50%, -50%);
    }


    
    .custom-button-hokkaidou {
      background: url('image/hokkaidou.svg');
      background-size: cover;
      width: 340px;
      height: 300px;
      color: white;
      border: none;
      font-size: 16px;

      position: absolute;
      top: 20%; /* 画像の上からの位置 (全体の30%) */
      left: 80%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }

    .custom-button-touhoku {
      background: url('image/touhoku.svg');
      background-size: cover;
      width: 220px;
      height: 320px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 48%; /* 画像の上からの位置 (全体の30%) */
      left: 70%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }

    .custom-button-kanntou {
      background: url('image/kanntou.svg');
      background-size: cover;
      width: 150px;
      height: 160px;
      color: white;
      border: none;
      font-size: 16px;
    background: transparent;

      position: absolute;
      top: 66%; /* 画像の上からの位置 (全体の30%) */
      left: 68%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }

    .custom-button-tyuubu {
      background: url('image/tyuubu.svg');
      background-size: cover;
      width: 134px;
      height: 330px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 63%; /* 画像の上からの位置 (全体の30%) */
      left: 54%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }

    .custom-button-kinnki {
      background: url('image/kinnki.svg');
      background-size: cover;
      width: 200px;
      height: 300px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 70%; /* 画像の上からの位置 (全体の30%) */
      left: 40%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }

    .custom-button-tyuugoku {
      background: url('image/tyuugoku.svg');
      background-size: cover;
      width: 180px;
      height: 130px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 69%; /* 画像の上からの位置 (全体の30%) */
      left: 24%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }


    .custom-button-shikoku {
      background: url('image/shikoku.svg');
      background-size: cover;
      width: 180px;
      height: 100px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 80%; /* 画像の上からの位置 (全体の30%) */
      left: 30%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }



    .custom-button-okinawa {
      background: url('image/okinawa.svg');
      background-size: cover;
      width: 150px;
      height: 150px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 47%; /* 画像の上からの位置 (全体の30%) */
      left: 16%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }



    .custom-button-kyuusyuu {
      background: url('image/kyuusyuu.svg');
      background-size: cover;
      width: 150px;
      height: 180px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 85%; /* 画像の上からの位置 (全体の30%) */
      left: 14%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }


    .h3dayo {
text-align: center;
display: flex;
justify-content: center;
font-weight: 500;
font-size: 25px;}
  </style>
  <p class="h3dayo"> 各県を案内します．興味のある<strong>エリア</strong>を選んでください．</p>
  <div class="image-container">
    <!-- 画像を表示 -->
    <!-- <img src="/path/to/your-image.jpg" alt="Sample Image" />
   -->

        <img src="/image/japan.jpg" alt="Japan Image" />

    <a href="/hokkaidou" class="custom-button-hokkaidou"></a>
    <a href="/touhoku" class="custom-button-touhoku"></a>
    <a href="/kanntou" class="custom-button-kanntou"></a>
    <a href="/tyuubu" class="custom-button-tyuubu"></a>
    <a href="/kinnki" class="custom-button-kinnki"></a>
    <a href="/shikoku" class="custom-button-shikoku"></a>
    <a href="/tyuugoku" class="custom-button-tyuugoku"></a>
    <a href="/kyuusyuu" class="custom-button-kyuusyuu"></a>
    <a href="/okinawa" class="custom-button-okinawa"></a>



    <!-- ボタン1を配置 -->
    <!-- <button class="button1" on:click={() => alert('Button 1 clicked!')}>Button 1</button> -->
  
    <!-- ボタン2を配置 -->
    
  </div>
  

