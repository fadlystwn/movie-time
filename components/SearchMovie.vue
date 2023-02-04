<template>
  <div class="relative z-10">
    <input class="rounded border border-gray-400 px-3 py-2 focus:outline-none focus:shadow-outline" type="text"
      placeholder="Search..." v-model="searchTerm" @input="handleInput" />
    <ul class="absolute w-full bg-white border border-gray-400 rounded text-gray-700 py-2" v-if="searchResults.length">
      <li v-for="result in searchResults" :key="result.id" class="px-3 py-2 hover:bg-gray-400"
        @click="handleClick(result)">
        {{ result.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchTerm: '',
      searchResults: [],
      allData: [
        {
          img: "https://via.placeholder.com/220x330.jpg",
          title: "The Godfather",
          year: 1972,
          popularity: 9
        },
        {
          img: "https://via.placeholder.com/220x330.jpg",
          title: "The Shawshank Redemption",
          year: 1994,
          popularity: 9
        },
        {
          img: "https://via.placeholder.com/220x330.jpg",
          title: "The Dark Knight",
          year: 2008,
          popularity: 9
        },
        {
          img: "https://via.placeholder.com/220x330.jpg",
          title: "Pulp Fiction",
          year: 1994,
          popularity: 8
        },
        {
          img: "https://via.placeholder.com/220x330.jpg",
          title: "The Lord of the Rings: The Return of the King",
          year: 2003,
          popularity: 8
        }
      ]
    }
  },
  methods: {
    handleInput() {
      this.searchResults = this.allData.filter(item => {
        return item.title.toLowerCase().includes(this.searchTerm.toLowerCase());
      });
    },
    handleClick(result) {
      this.searchTerm = result.title;
      this.searchResults = [];
    }
  }
}
</script>