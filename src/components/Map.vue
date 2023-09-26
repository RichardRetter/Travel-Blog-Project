<template>
  <div id="map" class="basemap"></div>
</template>

<script>
import mapboxgl from 'mapbox-gl';
export default {
  name: 'BaseMap',

  mounted() {
    mapboxgl.accessToken = import.meta.env.VITE_MY_API_KEY;

    const map = new mapboxgl.Map({
      container: 'map',
      style: 'mapbox://styles/mapbox/streets-v11',
      center: [2.3483915, 48.8534951],
      zoom: 1.5,
      hash: true
    });

    const popup = new mapboxgl.Popup()
      .setHTML(
        '<h3>Paris</h3> <h3>Visiting date: 2015.09.21</h3> <h3>Posted by Richard</h3> <a href="http://localhost:5173/details?name=Paris&image=https://cdn.wallpapersafari.com/95/17/jA06IS.jpg&visitingDate=2015.09.21">Click here for details</a>'
      )
      .setMaxWidth('300px');

    const popup2 = new mapboxgl.Popup()
      .setHTML(
        '<h3>San Diego</h3> <h3>Visiting date: 2017.08.17</h3> <h3>Posted by Richard</h3> <a href="http://localhost:5173/details?name=San%20Diego&image=https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTv8n226JKT5jY2PmoIiOdTqkzo4EGJYUGwHw&usqp=CAU&visitingDate=2017.08.17">Click here for details</a>'
      )
      .setMaxWidth('300px');

    const popup3 = new mapboxgl.Popup()
      .setHTML(
        '<h3>Sydney</h3> <h3>Visiting date: 2019.05.09</h3> <h3>Posted by Richard</h3> <a href="http://localhost:5173/details?name=Sydney&image=https://travel2next.com/wp-content/uploads/sydney-opera-house-at-night.jpg&visitingDate=2019.05.09">Click here for details</a>'
      )
      .setMaxWidth('300px');

    const popup4 = new mapboxgl.Popup()
      .setHTML(
        '<div><h3>Stockholm</h3> <h3>Visiting date: 2017.02.06</h3> <h3>Posted by Richard</h3> <a href="http://localhost:5173/details?name=Stockholm&image=https://upload.wikimedia.org/wikipedia/commons/e/e2/Stockholm_Skyline_At_Night_%2891983391%29.jpeg&visitingDate=2017.02.06">Click here for details</a></div>'
      )
      .setMaxWidth('300px');

    const popup5 = new mapboxgl.Popup()
      .setHTML(
        '<h3>Tokyo</h3> <h3>Visiting date: 2013.07.23</h3> <h3>Posted by Richard</h3> <a href="http://localhost:5173/details?name=Tokyo&image=https://assets.cntraveller.in/photos/60ba13c3556f29fbec5f2281/16:9/w_1920,h_1080,c_limit/Tokyo-Shibuya-neon-lights.jpg&visitingDate=2013.07.23">Click here for details</a>'
      )
      .setMaxWidth('500px');

    const popup6 = new mapboxgl.Popup()
      .setHTML(
        '<h3>Las Vegas</h3> <h3>Visiting date: 2014.07.12</h3> <h3>Posted by Richard</h3> <a href="http://localhost:5173/details?name=Las%20Vegas&image=https://vegasexperience.com/wp-content/uploads/2023/01/Photo-of-Las-Vegas-Downtown-1920x1280.jpg&visitingDate=2014.07.12">Click here for details</a>'
      )
      .setMaxWidth('300px');

    new mapboxgl.Marker().setLngLat([2.3483915, 48.8534951]).setPopup(popup).addTo(map);
    new mapboxgl.Marker().setLngLat([-117.162773, 32.71742]).setPopup(popup2).addTo(map);
    new mapboxgl.Marker().setLngLat([151.216454, -33.854816]).setPopup(popup3).addTo(map);
    new mapboxgl.Marker().setLngLat([18.071093, 59.325117]).setPopup(popup4).addTo(map);
    new mapboxgl.Marker().setLngLat([139.1485991, 35.76478424]).setPopup(popup5).addTo(map);
    new mapboxgl.Marker().setLngLat([-115.148516, 36.167256]).setPopup(popup6).addTo(map);
  }
};
</script>

<style scoped>
.mapboxgl-popup {
  cursor: pointer;
  max-width: 200px;
}

.mapboxgl-marker {
  cursor: pointer;
}

#map {
  color: black;
  width: 100%;
  height: 100%;
}
</style>
