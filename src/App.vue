<script>
export default {
  name: "app",

  data() {
    return {
      query: "",
    };
  },
};
</script>

<template>
  <div class="app">
    <main class="search_box">
      <input class="search" v-model="query" placeholder="Search here...." />
    </main>

    <div class="location">
      <div class="time">Los Angeles</div>
      <div class="date">Mon,23 July 2022</div>
    </div>
    {{ query }}
  </div>
  <div class="desktop-display">Not available on desktop</div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.desktop-display {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 4rem;
}
.search_box {
  display: none;
}

@media (max-width: 600px) {
  .app {
    background-image: url("./assets/weather-bg.avif");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    height: 100vh;
    padding: 2rem;
  }
  .search_box {
    display: flex;
    align-items: center;
    justify-content: center;
    display: unset;
  }
  .search {
    width: 100%;
    height: 40px;
    border: none;
    border-radius: 0 10px 0 10px;
    padding: 10px;
    outline: none;
  }
  .desktop-display {
    display: none;
  }
  .location {
    text-align: center;
    margin-top: 3rem;
    color: white;
    font-family: montserrat, sans-serif;
    padding: 10px;
  }
  .time {
    font-size: 2.5rem;
    padding-bottom: 10px;
    text-shadow: 2px 2px 5px black;
    letter-spacing: 1px;
  }
  .date {
    font-size: 1rem;
    text-shadow: 2px 2px 5px black;
    letter-spacing: 2px;
  }
}
</style>
