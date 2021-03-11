<template>
<div class="test">
      <MglMap :accessToken="accessToken" :mapStyle="mapStyle" :center="center" :zoom="zoom">
          <MglAttributionControl />
      <MglNavigationControl position="top-right" />
      <MglGeolocateControl position="top-right" />
      <MglNavigationControl position="top-right" />
      <MglGeolocateControl position="top-right" />
      <MglScaleControl />
      </MglMap>
</div>

</template>

<script>
import Mapbox from "mapbox-gl";
import { MglMap,      MglScaleControl, MglNavigationControl, MglGeolocateControl} from "vue-mapbox";

export default  {
    name:'Map',
  components: {
    MglMap,
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
    
    };
  },
    created() {
    
    // We need to set mapbox-gl library here in order to use it in template
    //this.addControl(new Mapbox.FullscreenControl());
    //Mapbox.addControl(new Mapbox.FullscreenControl());
    this.mapbox = Mapbox;
    
  },
  
  
};
</script>
<style lang="postcss" scoped>
test{
position: absolute; top: 0; bottom: 0; width: 100%;    
}
</style>


