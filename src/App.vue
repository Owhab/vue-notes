<script setup>
import "./assets/app.css";
</script>

<template>
  <div class="app">
    <pre>
      <!-- {{ notes }} -->
    </pre>
    <div class="header"><h1 class="app-title">Vue Notes</h1></div>
    <div class="contextbox">
      <input type="text" placeholder="Title" />
      <textarea
        rows="8"
        placeholder="Description"
        class=""
        spellcheck="false"
      ></textarea>
      <div class="controls">
        <div class="colors">
          <span class="c1" data-note-color="#D8E2DC"></span>
          <span class="c2" data-note-color="#FFE5D9"></span>
          <span class="c3" data-note-color="#FBFAF0"></span>
          <span class="c4" data-note-color="#FFE9EE"></span>
          <span class="c5" data-note-color="#FFDDE4"></span>
        </div>
        <button>Add</button>
      </div>
    </div>
    <div class="filter">
      <button>All (2)</button>
      <button style="background-color: rgb(216, 226, 220)">1</button>
      <button style="background-color: rgb(255, 229, 217)">0</button>
      <button style="background-color: rgb(251, 250, 240)">0</button>
      <button style="background-color: rgb(255, 233, 238)">0</button>
      <button style="background-color: rgb(255, 221, 228)">1</button>
      <button style="background-color: rgb(255, 255, 255)">0</button>
    </div>

    <div class="notes">
      <!-- Note start -->
      <div
        v-for="note in notes"
        :key="note.id"
        class="note"
        style="background-color: rgb(216, 226, 220)"
      >
        <div>
          <h3 class="title">very important note</h3>
          <p>heyyy</p>
        </div>
        <p class="time">a few seconds ago</p>
        <div class="buttons"><button class="delete">×</button></div>
      </div>
      <!-- note end -->
    </div>
  </div>  
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
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

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
