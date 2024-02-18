import { default } from '../../App.vue';
<template>
  <h1>Quien es ese pokemon?</h1>
  <PokemonPicture :pokemonId="180" :showPokemon="true" />
  <PokemonOptions />
</template>

<script>
import PokemonPicture from "@/components/PokemonPicture";
import PokemonOptions from "@/components/PokemonOptions";
import getPokemonOptions from "@/helpers/getPokemonOptions";

console.log(getPokemonOptions());

export default {
  name: "PokemonPage",
  components: {
    PokemonPicture,
    PokemonOptions,
  },
};
</script>

<style></style>
