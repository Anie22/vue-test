<template>
  <div class="home">
    <HelloWorld msg="Arrays"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },
}
</script>

<style scoped>
.hello{
  padding-top: 20px;
  padding-left: 20px;
}
.btn{
  background: hsl(276, 95%, 48%);
  color: hsl(0, 19%, 92%);
  text-align: center;
  height: 50px;
  width: 20%;
  margin: 1.2em;
  font-size: 18px;
  border-radius: 8px;
}
</style>