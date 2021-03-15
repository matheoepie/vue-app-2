<template>
  <div class="info">
    <h1>Liste des établissements</h1>
    <Datas></Datas>
  </div>
</template>
<script>

import Datas from '@/components/getdata.vue'

export default {
  name: 'info',
  components: {
    Datas
  }
}
</script>