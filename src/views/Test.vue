<template>
  <div class="test">
    <h1>This is an Test page</h1>
    <Datas></Datas>
  </div>
</template>
<script>
// @ is an alias to /src
import Datas from '@/components/getdata.vue'

export default {
  name: 'test',
  components: {
    Datas
  }
}
</script>