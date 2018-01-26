<template>
  <div class="cat-container">
    <div class="cat-list-container">
      <ul v-for="cat in cats" class="cats-list">
        <li class="cats-list-cat">
          {{ cat.name }} <button @click="addCat(cat)">+</button> <button @click="removeCat(cat)">-</button>
        </li>
      </ul>
    </div>
    <div class="cat-chosen">
      <h2>Thanks for adopting {{ chosenCat.name }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cats',
  data () {
    return {
      cats: [
        {id: 1, name: 'fegaro', furColor: 'black'},
        {id: 2, name: 'puru', furColor: 'white'}
      ],
      chosenCat: {}
    };
  },
  methods: {
    addCat (cat) {
      this.chosenCat = cat;
    },
    removeCat (cat) {
      this.chosenCat = {};
    }
  }
};
</script>

<style scoped>
  .cat-container {
    margin: 20px;
    display: flex;
    align-content: space-around;
  }

  .cats-list {
    list-style: none;
    text-align: center;
    width: 300px;
    margin-right: 500px;
  }

  .cats-list-cat {
    background-color: #555;
    border: 1px solid #dfdfdf;
  }

  button {
    width: 20px;
    height: 20px;
    margin: 5px;
  }
</style>
