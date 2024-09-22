<h1> <strong>四国</strong></h1><!-- src/routes/index.svelte -->
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
  


    .custom-button-ehime {
      background: url('image/prefecture/ehime.svg');
      background-size: cover;
      width: 450px;
      height: 460px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 50%; /* 画像の上からの位置 (全体の30%) */
      left: 30%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }


    .custom-button-kouti {
      background: url('image/prefecture/kouti.svg');
      background-size: cover;
      width: 500px;
      height: 350px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 60%; /* 画像の上からの位置 (全体の30%) */
      left: 53%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }



    .custom-button-tokusima {
      background: url('image/prefecture/tokusima.svg');
      background-size: cover;
      width: 320px;
      height: 270px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 31%; /* 画像の上からの位置 (全体の30%) */
      left: 78%; /* 画像の左からの位置 (全体の40%) */
      transform: translate(-50%, -50%); /* ボタンの中央を基準に調整 */
    }



    .custom-button-kagawa {
      background: url('image/prefecture/kagawa.svg');
      background-size: cover;
      width: 290px;
      height: 160px;
      color: white;
      border: none;
      font-size: 16px;
      background: transparent;
      position: absolute;
      top: 12%; /* 画像の上からの位置 (全体の30%) */
      left: 72%; /* 画像の左からの位置 (全体の40%) */
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

        <img src="/image/prefecture/sikoku_pre.jpg" alt="Japan Image" />

    <a href="/kagawa" class="custom-button-kagawa"></a>
    <a href="/tokusima" class="custom-button-tokusima"></a>
    <a href="/kouti" class="custom-button-kouti"></a>
    <a href="/ehime" class="custom-button-ehime"></a>
    <!-- <a href="/kinnki" class="custom-button-kinnki"></a>
    <a href="/shikoku" class="custom-button-shikoku"></a>
    <a href="/tyuugoku" class="custom-button-tyuugoku"></a>
    <a href="/kyuusyuu" class="custom-button-kyuusyuu"></a>
    <a href="/okinawa" class="custom-button-okinawa"></a> -->



    <!-- ボタン1を配置 -->
    <!-- <button class="button1" on:click={() => alert('Button 1 clicked!')}>Button 1</button> -->
  
    <!-- ボタン2を配置 -->
    
  </div>
  

