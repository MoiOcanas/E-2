<template>
  <div>
    <h1>My Favorite Artists</h1>
    <ol>
      <item-list v-for="art in artists" :art="art" :key="art.id"></item-list>
    </ol>
  </div>
</template>

<script>
import ItemList from "./components/ItemList.vue";
export default {
  name: "app",
  data() {
    return {
      artists: [
        { id: 0, name: "Daft Punk" },
        { id: 1, name: "Justice" },
        { id: 2, name: "Parcels" },
        { id: 3, name: "Jungle" },
        { id: 4, name: "Sir Sly" },
        { id: 5, name: "Gorillaz" },
        { id: 6, name: "Soulwax" },
        { id: 7, name: "Metallica" },
        { id: 8, name: "Little Jesus" },
        { id: 9, name: "Run the Jewels" }
      ]
    };
  },
  components: {
    ItemList
  }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Cabin');
$primary-color: black;
$secondary-color: #E9E9E9;
$third-color: #f9f9f9;

body {
  background: $third-color;

  h1 {
    text-align: center;
    font-family: 'Cabin', sans-serif;
    font-size: 4em;
  }

  ol {
    background: $secondary-color;
    margin: 0 auto;
    border-radius: 2px;
    width: 800px;
    padding: 5px;
    list-style: none;

    display: grid;
    grid-template-rows: auto auto auto;
  }
}
</style>
