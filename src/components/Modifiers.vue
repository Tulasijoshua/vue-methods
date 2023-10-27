<template>
  <div>
    <h2 v-once>{{ name }}</h2>
    <button @click="name = 'Tulasi'">Change name</button>
    <h2 v-pre>{{name}}</h2>
  </div>
</template>

<script>
export default {
    data() {
        return {
            name: 'Joshua'
        }
    }
}
</script>

<style>

</style>