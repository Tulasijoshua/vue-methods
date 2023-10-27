<template>
  <div class="">
    <h2>Volume Tracker (0-20)</h2>
    <h2>Volume - {{volume}}</h2>
    <button @click="volume += 2">Increment</button>
    <button @click="volume -= 2">Decrement</button>

    <div>
      <div>
        <pre>
          {{ JSON.stringify(movieInfo, null, 2) }}
        </pre>
      </div>
      <input type="text" v-model="movie" />
      <input type="text" v-model="movieInfo.title" />
      <input type="text" v-model="movieInfo.actor" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      volume: 0,
      movie: 'Caleb',
      movieInfo: {
        title: '',
        actor: '',
      }
    }
  },
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 18) {
        alert('Listening at this volume can cause damage!');
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with movie name ${newValue}`)
      },
      immediate: true
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Calling API with title ${newValue.title} and actor ${newValue.actor}`)

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