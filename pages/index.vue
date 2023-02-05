<template>
  <Layout>
    <section class="bg-gray-900 pt-10">
      <VueSlickCarousel :dots="true" v-bind="slickOptions">
        <MoviePoster />
        <MoviePoster />
        <MoviePoster />
        <MoviePoster />
        <MoviePoster />

      </VueSlickCarousel>
    </section>
    <section class="bg-gray-800 pt-10 container mx-auto">
      <div class="flex justify-between">
        <h3 class="text-base">Discover Movies</h3>
        <div class="flex">
          <button role="button"
            class="text-sm ml-3 p-2 px-4 rounded-full bg-red hover:bg-red-700 text-white">Popularity</button>
          <button role="button" class="text-sm ml-3 p-2 px-4 rounded-full  bg-black hover:bg-red-700 text-white">Release
            Date</button>
        </div>
      </div>
      <MovieList />

    </section>

  </Layout>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
import MovieList from '../components/MovieList.vue'
import Layout from '../layout/layout.vue'
export default {
  data() {
    return {
      slickOptions: {
        centerMode: true,
        centerPadding: "360px",
        focusOnselect: true,
        speed: 500,
        slidesToShow: 1,
        scrollToShow: 3,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              centerPadding: "200px",
              slidesToShow: 1,
              slidesToScroll: 1
            }
          },
          {
            breakpoint: 600,
            settings: {
              centerPadding: "20px",
              slidesToShow: 1,
              slidesToScroll: 1
            }
          },
          {
            breakpoint: 480,
            settings: {
              centerPadding: "100px",
              slidesToShow: 1,
              slidesToScroll: 1
            }
          }
        ]
      },
    }
  },
  name: 'IndexPage',
  components: { VueSlickCarousel, MovieList, Layout },
}
</script>
