<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">pwa-base-app-v2</h1>
      <h2 class="subtitle">My wicked Nuxt.js projects YEAH!!</h2>
      <div class="actions">
        <a @click="addTada">🎉 {{ tada }}</a>
        <a @click="addSparkles">✨ {{ sparkles }}</a>
        <a @click="addThumbsup">👍 {{ thumbsup }}</a>
        <a @click="addHeart">🧡 {{ heart }}</a>
        <a @click="clear">Clear</a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {
      tada: 0,
      sparkles: 0,
      thumbsup: 0,
      heart: 0
    }
  },
  methods: {
    addTada() {
      this.tada++
    },
    addSparkles() {
      this.sparkles++
    },
    addThumbsup() {
      this.thumbsup++
    },
    addHeart() {
      this.heart++
    },
    clear() {
      this.tada = 0
      this.sparkles = 0
      this.thumbsup = 0
      this.heart = 0
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
