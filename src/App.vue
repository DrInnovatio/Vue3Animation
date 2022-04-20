<template>
<button type="button" @click="flag = !flag">Toggle</button>
<transition name="fade">
  <h2 v-if="flag">Hello Habok!!</h2>
</transition>
</template>

<script>
export default {
  name: "App",
  data(){
    return{
      flag: false,
    }
  }
};
</script>

<style>
.fade-enter-from{
  opacity: 0;
}

.fade-enter-active {
  transition: all 2s linear; 
}

.fade-leave-to {
  transition: all 2s linear;
  opacity: 0;
}
</style>
