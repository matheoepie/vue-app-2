
<template>
<div class="map">
  <Map/>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
<link href='https://api.mapbox.com/mapbox-gl-js/v2.1.1/mapbox-gl.css' rel='stylesheet' />
  </div>
<script src='https://api.mapbox.com/mapbox-gl-js/v2.1.1/mapbox-gl.js'></script>
</div>
  
</template>

<script>
import Map from "../components/Map";

export default  {
    name:'map',
    components: {
    Map
    
   }
  };
</script>
<style >
map{
     position: absolute; top: 0; bottom: 0; width: 100%; height: 100%;
}
</style>
