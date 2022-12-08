<script setup>
</script>

<template>
  <div class="app">
    <h1>Cookie Clicker</h1>
    <button @click="click()">Click me</button>
    <p>Count: {{ clicks }}</p>
    <button @click="buy_1inc()">Buy extra click</button>
    <button @click="buy_10inc()">Buy 10 extra clicks</button>
    <button @click="buy_100inc()">Buy 100 extra clicks</button>
    <button @click="buy_max()">Buy max extra clicks</button>
  </div>
</template>

<script>
export default {
  data() {
    const clicks = 0
    const click_inc = 1
    return { clicks, click_inc }
  },
  methods: {
    click() {
      this.clicks += this.click_inc
      console.log(this.clicks)
    }, 
    buy_1inc() {
      if (this.clicks > 9) {
        this.click_inc += 1
        this.clicks -= 10
      }
    },
    buy_10inc() {
      if (this.clicks > 99) {
        this.click_inc += 10
        this.clicks -= 100
      }
    },
    buy_100inc() {
      if (this.clicks > 999) {
        this.click_inc += 100
        this.clicks -= 1000
      }
    },
    buy_max() {
      while (this.clicks > 9) {
        if (this
      }
    }
  }
}
</script>

<style scoped>
.app {
  text-align: center;
}

h1 {
  font-size: 40px;
  font-weight: normal;
  margin: 20px 0;
}

button {
  font-size: 20px;
  padding: 10px 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background: #fff;
  cursor: pointer;
}

button:hover {
  background: #eee;
}

</style>
