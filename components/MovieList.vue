<template>
  <div class="text-white">
    <div class="columns-5 gap-4 my-4">
      <div v-for="item in items" v-bind:key="item.id">
        <template class="flex flex-col rounded">
          <img class="w-full" :src="item.img" alt="" />
          <p>{{ item.title }}</p>
          <p>{{ item.year }}</p>
        </template>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
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
  }
}
</script>
