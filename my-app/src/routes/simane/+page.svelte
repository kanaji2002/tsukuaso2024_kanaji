<script>
  import { onMount } from 'svelte';

  let map;

  onMount(() => {
    // Google Maps APIのスクリプトを動的に読み込む
    const script = document.createElement('script');
    script.src = `https://maps.googleapis.com/maps/api/js?key=AIzaSyDZPeR7vFlw3DKxx-mxKifxrA48oWtzt-U&callback=initMap`;
    script.async = true;
    document.head.appendChild(script);



    const baseLat = 	35.47222;
    const baseLng = 	133.05056;
    // 地図を初期化する関数
    window.initMap = () => {
      const latlng = new google.maps.LatLng(baseLat, 	baseLng);

      const myOptions = {
        zoom: 10,
        scrollwheel: false,
        streetViewControl: false,
        center: latlng,
        mapTypeControlOptions: { mapTypeIds: ['style', google.maps.MapTypeId.ROADMAP] }
      };

      // 地図を表示する要素
      map = new google.maps.Map(document.getElementById('js-access-map'), myOptions);

      // 複数のピンを設置する座標のリスト

      const variation = 0.1;

      const locations = [
        { lat: baseLat + (Math.random() * variation * 2 - variation), lng: baseLng + (Math.random() * variation * 2 - variation), title: 'サンプル1' },
        { lat: baseLat + (Math.random() * variation * 2 - variation), lng: baseLng + (Math.random() * variation * 2 - variation), title: 'サンプル2' },
        { lat: baseLat + (Math.random() * variation * 2 - variation), lng: baseLng + (Math.random() * variation * 2 - variation), title: 'サンプル3' },
        { lat: baseLat + (Math.random() * variation * 2 - variation), lng: baseLng + (Math.random() * variation * 2 - variation), title: 'サンプル4' },
        { lat: baseLat + (Math.random() * variation * 2 - variation), lng: baseLng + (Math.random() * variation * 2 - variation), title: 'サンプル5' }
      ];

      // カスタムアイコン
      const icon = {
        url: 'image/pin.png', // アイコンの画像URLを指定
        scaledSize: new google.maps.Size(40, 80) // アイコンのサイズを指定
      };

      // 各座標にマーカーを作成
      locations.forEach((location) => {
        const markerOptions = {
          position: new google.maps.LatLng(location.lat, location.lng),
          map: map,
          title: location.title,
          icon: icon // カスタムアイコンを使用
        };
        new google.maps.Marker(markerOptions);
      });

      // 地図のスタイルをカスタマイズ（白黒の例）
      const styleOptions = [
        {
          'stylers': [
            { 'gamma': 0.8 },
            { 'saturation': 60 },
            { 'lightness': 20 }
          ]
        }
      ];

      const styledMapOptions = { name: 'サンプル' };
      const originalType = new google.maps.StyledMapType(styleOptions, styledMapOptions);
      map.mapTypes.set('style', originalType);
      map.setMapTypeId('style');
    };
  });



// ポップアップを表示する関数
function showPopup() {
document.getElementById("popup").style.display = 'block';
}

// SvelteのonMountフックを使用して、ページロード後に処理を実行
onMount(() => {
setTimeout(() => {
  showPopup(); // 5秒後にポップアップを表示
}, 3000);
});

// ポップアップを閉じる関数
function closePopup() {
document.getElementById("popup").style.display = 'none';
}

</script>

<h1>島根のおすすめスポット</h1>

<div id="js-access-map" style="height: 700px; width: 100%;"></div>


<div id="popup" class="popup">
  <img src="/image/maiko/simane.png" alt="ポップアップの画像">
  <h1><strong>京都においでやす．</strong></h1>
  <button class="close-button" on:click={closePopup}>閉じる</button>
</div>

<style>
  .popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 700px;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    z-index: 1000;
    text-align: center;
    border-radius: 10px;
  }

  .popup img {
    width: 100%;
    height: auto;
    margin-bottom: 15px;
  }

  .close-button {
    padding: 10px 20px;
    background-color: #ff4444;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  .close-button:hover {
    background-color: #cc0000;
  }

  </style>