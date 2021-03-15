<template>
    <div id="Datas">
        {{ info }}
    </div>
</template>
<script>
import axios from 'axios';
export default {
    name:"Datas",
    data () {
        return{
            info: null    
        }
        
    },
    mounted () {
    axios
      .get('https://data.loire-atlantique.fr/api/records/1.0/search/?dataset=224400028_lieux-numeriques-en-loire-atlantique')
      .then(response => (this.info = response.data.records))
  }
}
</script>
