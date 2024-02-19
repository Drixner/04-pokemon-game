<template>
  <h1>Quien es ese pokemon?</h1>
  <PokemonPicture :pokemonId="180" :showPokemon="true" />
  <PokemonOptions :pokemons="pokemonArr" />
</template>

<script>
import PokemonPicture from "@/components/PokemonPicture";
import PokemonOptions from "@/components/PokemonOptions";
import getPokemonOptions from "@/helpers/getPokemonOptions";

// console.log(getPokemonOptions());

export default {
  name: "PokemonPage",
  components: {
    PokemonPicture,
    PokemonOptions,
  },
  data() {
    return {
      pokemonArr: [],
    };
  },
  methods: {
    async mixPokemonArray() {
      this.pokemonArr = await getPokemonOptions();
      console.log(this.pokemonArr);
    },
  },
  mounted() {
    this.mixPokemonArray();
  },
};
</script>

<style></style>
