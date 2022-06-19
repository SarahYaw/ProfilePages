<template>
  <h2>[Name] Family Genealogy</h2>
  <h3>Hello! Welcome to the [name] family genealogy database!</h3>
  <p>Search by Name</p>
  <!-- search bar -->
  <p>Search by Year</p>
  <!-- number entry -->
  <p>Randomly choose a record</p>
  <!-- button -->
  <button @click="randomize">Random Person</button>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
    isHomePage: true,
    }
  },
  computed: {
    
  },
  methods: {
    onBeforeMount() {
      this.isHomePage = true;
    },
    toggleHome() {
      console.log("isHomePage",this.isHomePage)
      this.isHomePage = !this.isHomePage;
    },
    randomize() {
      this.toggleHome();
    }
  },
  components: {

  }
}
</script>

<style>
@import "./assets/main.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
