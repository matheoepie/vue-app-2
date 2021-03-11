
<template>
<div class="map">
  <Map/>
</div>
  
</template>

<script>
import Map from "../components/Map";

export default  {
    name:'Beb',
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
