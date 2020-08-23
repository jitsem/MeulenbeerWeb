<template>
  <div class="container">
    <div class="fancy-list">
        <ul>
          <li v-for="beer in beers" v-bind:key="beer.id">
            <div class="beer-link"  v-bind:class="{'beer-link-selected' : isSelected(beer.id)}" 
            @click="changeBeer(beer.id)">
                <h4>{{ beer.title }}</h4>
            </div>
          </li>
        </ul>
    </div>
    <div class="beer-details">
      <Beer v-bind:beer="selectedBeer" />
    </div>
  </div>
</template>

<script>
import Beer from "./Beer";
export default {
  name: "BeerList",
  components: {
    Beer,
  },
  props: ["beers"],
  data() {
    return {
      selectedBeer: {},
    };
  },
  methods: {
    changeBeer(id) {
      console.log(id);
      this.selectedBeer = this.beers.find((b) => b.id === id);
    },
    isSelected(id) {
      return this.selectedBeer != null && this.selectedBeer.id === id;
    },
  },
};
</script>

<style scoped>
.container {
    display: flex;
    border: #2aa9f4 1px solid;
    background-color: #d4d4d4;
}

.fancy-list li{
    list-style: none;
}

.beer-link{
    width: 100%;
    min-width: 150px;
    min-height: 50px;
    border: #c1c1c1 2px solid;
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
}
.beer-link:hover{
    border: #b1b1b1 4px solid;
}

.beer-link-selected{
    border: #b1b1b1 4px solid;
    background-color: #fee715;
}

.beer-details
{
    margin: 10px 15px;
    
}
</style>