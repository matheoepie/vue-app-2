<template>
  <div class="test">
    <h1>This is an Test page</h1>
    <TestComponnent msg="TestOuia"/>
  </div>
</template>
<script>
// @ is an alias to /src
import TestComponnent from '@/components/TestComponnent.vue'

export default {
  name: 'test',
  components: {
    TestComponnent
  }
}
</script>