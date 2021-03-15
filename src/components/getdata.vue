<template>
    <div id="Datas">
        <div id="app">
            <div v-bind:key="Datas" v-for="Datas in info">
                <v-card max-width="400"> 
                    <div class="card">
                        <div class="container">
                            <h4><b>{{ Datas.fields.nom_lieu }}</b></h4>
                            <p>{{ Datas.fields.descriptif }}</p>
                            <p>Téléphone : {{ Datas.fields.telephone  }}</p>
                            <p>{{ Datas.fields.location }}</p>
                        </div>
                    </div>
                </v-card>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios';
export default {
    name:"Datas",
    data () {
        return{
            info: []    
        }
        
    },
    mounted () {
    axios
      .get('https://data.loire-atlantique.fr/api/records/1.0/search/?dataset=224400028_lieux-numeriques-en-loire-atlantique')
      .then(response => (this.info = response.data.records))
  }
}
</script>
<style scoped>
.card {
   box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  border-radius: 5px; 
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
}   
</style>

