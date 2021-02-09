<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <TestComponnent msg="Projet de Mathéo">
  </div>
</template>

<script>
// @ is an alias to /src
import TestComponnent from '@/components/TestComponnent.vue'
import TestComponnent from '../components/TestComponnent.vue'

export default {
  name: 'Home',
  components: {
    TestComponnent
  }
}
</script>
