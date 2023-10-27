<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Forms from './components/Forms.vue'
import Modifiers from './components/Modifiers.vue'
import ComputedProperties from './components/ComputedProperties.vue'
import Watchers from './components/Watchers.vue'
import Practice from './components/Practice.vue'
</script>

<template>
  <div :style="{
    width: '80%',
    margin: '0 auto',
    display: 'flex',
    justifyContent: 'spaceBetween'
  }">
  <!-- <HelloWorld  /> -->
  <!-- <Forms /> -->
  <Modifiers />
  <!-- <ComputedProperties /> -->
  <!-- <Watchers /> -->
  <Practice />
    
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.flexing {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
