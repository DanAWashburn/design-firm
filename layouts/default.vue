<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Electrolize|Farro&display=swap');

h1 {
  font-size: 500%;
  font-family: $title;
  color: $darkgrey;
}
</style>

<template>
<div id="app">
  <div class="container">
    <div class="flex-item-standard">
      <h1>design firm</h1>
    </div>
  </div>
  <div class="container">
    <nav class="flex-item2">

        <h5 class="list-inline-item">
          <n-link class="nav-link" to="/">Home</n-link>
        </h5>
        <h5 class="list-inline-item">
          <n-link class="nav-link" to="/team">Team</n-link>
        </h5>
        <h5 class="list-inline-item">
          <n-link class="nav-link" to="/press">Press</n-link>
        </h5>
        <h5 class="list-inline-item">
          <n-link class="nav-link" to="/drinks">Drinks</n-link>
        </h5>
    </nav>
  </div>
  <nuxt />
</div>
</template>
