<template>
  <div>
    <router-link to="/">Return Home</router-link>
    <h1>Our Beers</h1>
    <Beerlist v-bind:beers="beers"/>
  </div>
</template>

<script>
import Beerlist from '../components/BeerList'
export default {
    name: 'Beers',
    components: {
        Beerlist
    },
    data() {
        return {
            beers: [
                {
                    id: 1,
                    title: "Blond Oaked",
                    description: "This is the blond oaked, Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore",
                },
                {
                    id: 2,
                    title: "Golden Smash",
                    description: "This is the golden smash, Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore",
                },
                {
                    id: 3,
                    title: "Bitter Hop",
                    description: "This is the bitter hop, Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore",
                },
            ]
        }
    }
}
</script>