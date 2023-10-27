
<template>
  <div>
    <h2>{{ 5 + 30 + 5 }}</h2>
    <h2>Add method - {{ add(2, 4, 5) }}</h2>
    <h2>Add method - {{ add(20, 2, 15) }}</h2>
    <h2>Multiply method - {{ multiply(baseValue) }}</h2>
    <h2>{{ name }}</h2>
    <div>
      <button v-on:click="changeName($event), increment(2, $event)">Change name</button>
      <button v-on:mouseover="name = 'Tulasi'">Change name</button>
    </div>
    <h2>{{count}}</h2>
    <div>
      <button v-on:click="count += 1">Increment</button>
      <button v-on:click="count -= 1">Decrement</button>
    </div>
    <div>
      <button v-on:click="increment(1, $event)">Increment 1</button>
      <button @click="increment(5)">Increment 5</button>
      <button v-on:click="decrement(1)">Decrement 1</button>
      <button @click="decrement(5)">Decrement 5</button>
    </div>
  </div>
</template>

  <script>
    export default {
      data() {
        return {
          baseMultiplier: 5,
          baseValue: 3,
          name: 'Joshua',
          count: 0,
        }
      },
      methods: {
        changeName(event) {
          this.name = 'Mbawini'
          console.log('Event', event)
        },
        add(a, b, c) {
          return a + b + c
        },
        multiply(num) {
          return num * this.baseMultiplier
        },
        increment(num, event) {
          this.count += num
          console.log('Event', event)
        }, 
        decrement(num) {
          this.count -= num
        }
      }
    }
  
  </script>
<style scoped>
.read-the-docs {
  color: #888;
}
</style>
