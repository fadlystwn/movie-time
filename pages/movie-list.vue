
<template>
  <Layout>
    <section class="container m-auto">
      <div class="p-4">
        <h2 class="text-2xl font-medium border-t-6 border-red-500">Movies</h2>
      </div>
      <div class="flex flex-col md:flex-row">
        <div class="w-full md:w-1/4 p-4 bg-black">
          <div class="mb-4 ">
            <label class="text-white font-medium py-4">Sort Result by:</label>
            <select
              class="block appearance-none w-full bg-gray-700 border border-gray-800 text-white py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-gray-600 focus:border-gray-500"
              v-model="selectedSortOption">
              <option v-for="sortOption in sortOptions" :value="sortOption.value" v-bind:key="sortOption.id">{{
                sortOption.label
              }}</option>
            </select>
            <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
              <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                <path
                  d="M9.293l-3.536 3.536a1 1 0 0 0 1.414 1.414L10 11.414l3.536 3.536a1 1 0 0 0 1.414-1.414l-4-4a1 1 0 0 0-1.414 0l-4 4a1 1 0 0 0 1.414 1.414L9.293l3.536 3.536a1 1 0 0 0 1.414-1.414l-4-4a1 1 0 0 0-1.414 0l-4 4a1 1 0 0 0 1.414 1.414L9.293z" />
              </svg>
            </div>
          </div>
          <div class="px-6">
            <h3 class="text-lg font-medium">Genre</h3>
            <ul>
              <li v-for="genre in genres" :key="genre.id">
                <input type="checkbox" :value="genre.id" v-model="selectedGenres" />
                {{ genre.name }}
              </li>
            </ul>
          </div>
        </div>
        <div class="w-full md:w-3/4 p-4">
          <!-- Main content here -->
          <MovieList />
          <div class="text-center">
            <button class="bg-red-500 hover:bg-red-600 text-white font-medium py-2 px-10 rounded-full">
              Load More
            </button>
          </div>
        </div>
      </div>
    </section>
</Layout>
</template>
<script>
import Layout from '../layout/index.vue'
import MovieList from '../components/MovieList.vue'
export default {
  components: { Layout, MovieList },
  data() {
    return {
      selectedSortOption: '',
      sortOptions: [
        {
          id: 'sort01',
          label: 'Popularity',
          value: 'popularity'
        },
        {
          id: 'sort02',
          label: 'A-Z',
          value: 'a-z'
        },
        {
          id: 'sort03',
          label: 'Z-A',
          value: 'z-a'
        }
      ],
      genres: [
        { id: 1, name: 'Action' },
        { id: 2, name: 'Drama' },
        { id: 3, name: 'Comedy' },
        // add more genres here
      ],
      selectedGenres: []
    }
  },
}
</script>


