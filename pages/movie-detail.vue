<template>
  <div>
    <div class="relative bg-cover"
      style="background-image: url('https://via.placeholder.com/1240x480.jpg'); height: 480px">
      <div class="absolute top-0 right-0 left-0 bottom-0 bg-black bg-opacity-75"></div>
      <div class="absolute bottom-0 left-0 p-4">
        <h2 class="text-white text-2xl font-medium">{{ movie.title }}</h2>
        <p class="text-white text-sm">{{ movie.releaseYear }}</p>
        <p class="text-white text-sm">{{ movie.genres }}</p>
      </div>
      <div class="absolute top-0 left-0">
        <img :src="movie.thumbnail" alt="movie poster" />
      </div>

    </div>
    <div class="flex flex-col md:flex-row">
      <div class="w-full md:w-1/2 px-4 py-6">
        <div class="flex flex-col mb-4" v-for="review in reviews" v-bind:key="review.key">
          <div class="relative">
            <img class="w-32 h-32 rounded-full" :src="review.thumbnail" />
          </div>
          <div class="text-center mt-4">
            <div class="text-xl font-medium">{{ review.rating }}</div>
            <div class="text-gray-600">{{ review.username }}</div>
          </div>
        </div>
      </div>
      <div class="w-full md:w-1/2 px-4 py-6">
        <div class="flex flex-col mb-4" v-for="review in reviews" v-bind:key="review.id">
          <div class="text-xl font-medium">{{ review.title }}</div>
          <div class="text-gray-600">{{ review.review }}</div>
          <a class="underline" href="#">Read more</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      movie: {
        title: 'The Shawshank Redemption',
        releaseYear: 1994,
        genres: 'Drama',
        thumbnail: 'https://via.placeholder.com/220x330.jpg'
      },
      reviews: [
        {
          key: 1,
          thumbnail: 'https://via.placeholder.com/64.jpg',
          username: 'Jane Doe',
          rating: 4.5,
          title: 'Great Movie!',
          review: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
        },
        {
          key: 2,
          thumbnail: 'https://via.placeholder.com/64.jpg',
          username: 'John Doe',
          rating: 3.5,
          title: 'Good Movie',
          review: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
        },
        // add more reviews here
      ]
    }
  }
}
</script>