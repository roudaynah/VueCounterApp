<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods:{
    change(amount){
      this.count = this.count + amount
    }
  }
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
    </div>
  </header>
  <main>
    <p>Welcome to Counter App...</p>
    <button @click="change(-1)">-</button>
    <span>{{count}}</span>
    <button @click="change(1)">+</button>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
