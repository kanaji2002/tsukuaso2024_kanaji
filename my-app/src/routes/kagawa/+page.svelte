<script>
    import { onMount } from 'svelte';
  
    let map;
  
    onMount(() => {
      // Google Maps APIのスクリプトを動的に読み込む
      const script = document.createElement('script');
      script.src = `https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap`;
      script.async = true;
      document.head.appendChild(script);
  
      // 地図を初期化する関数
      window.initMap = () => {
        const latlng = new google.maps.LatLng(34.3428, 134.0466);
  
        const myOptions = {
          zoom: 18,
          scrollwheel: false,
          streetViewControl: false,
          center: latlng,
          mapTypeControlOptions: { mapTypeIds: ['style', google.maps.MapTypeId.ROADMAP] }
        };
  
        // 地図を表示する要素
        map = new google.maps.Map(document.getElementById('js-access-map'), myOptions);
  
        // マーカーを設定
        const markerOptions = {
          position: latlng,
          title: 'サンプル'
        };
        const marker = new google.maps.Marker(markerOptions);
        marker.setMap(map);
  
        // 地図のスタイルをカスタマイズ（白黒の例）
        const styleOptions = [
          {
            'stylers': [
              { 'gamma': 0.8 },
              { 'saturation': -100 },
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
  </script>
  
  <h1>香川</h1>
  
  <div id="js-access-map" style="height: 400px; width: 100%;"></div>
  