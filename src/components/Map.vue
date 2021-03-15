<template>

  <div class="map">
      <MglMap :accessToken="accessToken" :mapStyle="mapStyle" :center="center" :zoom="zoom" :list="list">
          <MglAttributionControl />
      <MglNavigationControl position="top-right" />
      <MglGeolocateControl position="top-right" />
      <MglNavigationControl position="top-right" />
      <MglGeolocateControl position="top-right" />
      <MglScaleControl />
      <MglMarker :coordinates="[	-1, 	50]" color="blue" />
      

      </MglMap>
</div>



</template>

<script>
import Mapbox from "mapbox-gl";
import { MglMap,  MglMarker,    MglScaleControl, MglNavigationControl, MglGeolocateControl} from "vue-mapbox";
import axios from 'axios';

export default  {
    name:'Map',
  components: {
    MglMap,
    MglMarker,
    MglNavigationControl,
    MglGeolocateControl,
    MglScaleControl
  },
  data() {
    return {
      accessToken: "pk.eyJ1IjoibWF0aGVvZXBpZSIsImEiOiJja20xc2x4em4yMTFvMm9vNjUzY2E3NXR1In0.ZzbK3oyGMWBZOZPJ6fCXsw", // your access token. Needed if you using Mapbox maps
      mapStyle:"mapbox://styles/matheoepie/ckm1spm4z08zi17k5fahzzzfm",
      center: [	-1.553621, 	47.218371],
      zoom: 10.15,
      popupCoordinates: [	-1.553621, 	47.248371],
      list: []
    
    };
  },mounted () {
    axios
      .get('https://data.loire-atlantique.fr/api/records/1.0/search/?dataset=224400028_lieux-numeriques-en-loire-atlantique')
      .then(response => (this.list = response.data.records))
  },
    created() {

    this.mapbox = Mapbox;
    
  }
  
  
};

</script>
<style lang="postcss" scoped>
.map{
  width: 100%;    
}
.marker {
  
  background-size: cover;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  cursor: pointer;
}
</style>


