<template>
<div>
 <article class="card">
	 <img :src="drink.strDrinkThumb"  class="card__img">
	 <h3 class="cocktail__title">{{ drink.strDrink }}</h3>
	 <p class="glass">{{ drink.strGlass }}</p>
   <p v-show="isShowing" class="cocktail__ingredient1">{{ drink.strIngredient1 }}</p>
   <p v-show="isShowing" class="cocktail__ingredient2">{{ drink.strIngredient2 }}</p>
   <p v-show="isShowing" class="cocktail__ingredient3">{{ drink.strIngredient3 }}</p>
   <p v-show="isShowing" class="cocktail__ingredient4">{{ drink.strIngredient4 }}</p>
   <p v-show="isShowing" class="cocktail__ingredient5">{{ drink.strIngredient5 }}</p>
   <p v-show="isShowing" class="cocktail__instructions">{{ drink.strInstructions }}</p>
   <b-button @click="toggleShow" href="#" variant="primary">Click to toggle information</b-button>
   <!--Put in more info with toggle/show and draw from toggle mixin. Start with v-show="!isShowing". See Picture.vue-->
 </article>

</div>
</template>

<script>
import {
  toggle
} from "./mixins/toggle.js";

export default {
	props: {
		drink: Object
	},

    mixins: [toggle],

    data() {
      return {
        isShowing: false
      };
    }
};
</script>


<style lang="scss">
.card {
	margin: 1rem;
	border: 1px solid #000;
	padding: 1.5rem;
	max-width: 200px;
	min-height: 200px;
	&__img {
		display: block;
		margin-bottom: 1rem;
    width: 150px;
	}
	&__title {
		font-size: 1rem;
		margin-bottom: .25rem;
	}
	&__copy {
		font-size: .875rem;
	}
}
</style>
