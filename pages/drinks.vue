<template>
  <div class="wrapper">
    <div class="container">
      <!--Why aren't the below centering?-->
      <h2 class="heading">Cocktails that Begin with "A"</h2>
      <h3 class="heading">"Architecture" isn't the only good thing that begins with "a."</h3>
    </div>
    <section class="zone">
        <cocktail
          v-for="drink in info"
          :key="drink.id"
          :drink="drink"
        />
    </section>
  </div>
</template>

<script>
import axios from 'axios';
import Cocktail from '~/components/Cocktail.vue';
//DO THIS

export default {
  components: {
    Cocktail
  },
  data () {
    return {
      info: null,
      loading: true,
      errored: false
    }
  },
  head () {
    return {
      title: this.title,
      meta: [
  { hid: 'design firm architects and drinks', name: 'drinnks from design firm', content: 'Some wonderful things that begin with "A".' }
      ]
    }
  },

  mounted () {
    axios
      .get('https://www.thecocktaildb.com/api/json/v1/1/search.php?f=a')
      .then(response => (this.info = response.data.drinks))
      .catch(error => {
        console.error(error)
        this.errored = true
      })
      .finally(() => this.loading = false)

  }
}
</script>

<style>
.zone {

  max-width: 1200px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  text-align: center;
  flex-wrap: wrap;
}




.links {
  padding-top: 15px;
}
</style>
