<template>
  <div class="relative">
    <button @click="isOpen = !isOpen" class="flex items-center">
      Categories
      <img src="path/to/arrow-down.png" class="w-4 h-4" v-if="!isOpen" />
      <img src="path/to/arrow-up.png" class="w-4 h-4" v-if="isOpen" />
    </button>
    <ul v-if="isOpen" class="absolute z-10 bg-white py-2 rounded-lg shadow-lg">
      <li v-for="item in items" class="px-4 py-2 hover:bg-gray-200 text-black" v-bind:key="item.id">
        {{ item.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
      items: [
        {
          id: 1,
          name: 'Action'
        },
        {
          id: 2,
          name: 'Drama'
        },
        {
          id: 3,
          name: 'Comedy'
        },
        {
          id: 4,
          name: 'Thriller'
        },
        {
          id: 5,
          name: 'Adventure'
        },
        {
          id: 6,
          name: 'Fantasy'
        },
        {
          id: 7,
          name: 'Science Fiction'
        },
        {
          id: 8,
          name: 'Romance'
        },
        {
          id: 9,
          name: 'Animation'
        },
        {
          id: 10,
          name: 'Horror'
        },
        {
          id: 11,
          name: 'Mystery'
        }
      ]
    }
  }
}
</script>