<template>
  <div >
    <h2>Volum tracker (0 - 20)</h2>
    <h2>Current volume - {{ volume }}</h2>
    <button v-on:click="increment">Increment</button>
    <button v-on:click="decrement">decrement</button>

    <input type="text" v-model="movie" />

    <input type="text" v-model="movieInfo.title">
    <input type="text" v-model="movieInfo.actor">

    <button v-on:click="movieList = movieList.concat(['Spiderman'])">Add movie</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      movieInfo: {
        actor: '',
        title: '',
      },
      movieList: ['Superman', 'Avengers']
    }
  },
  methods: {
    increment() {
      this.volume += 2
    },
    decrement() {
      this.volume -= 2
    },
  },
  watch: {
    volume(newValue, oldValue) {
      if(newValue > oldValue && newValue === 16) {
        alert('Listening at high volume may damage your hearing!!!')
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with movie name = ${newValue}`)
      },
      immediate: true
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`)
      },
      deep: true
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated list ${newValue}`)
      },
      deep: true
    }
  }
}
</script>

<style>
  .marTop {
    margin-top: 5rem;
  }
</style>. 