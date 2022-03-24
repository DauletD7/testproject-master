<template>
  <div>
    <div class="bg-black text-white">
      <div class="container mx-auto">
        <div class="flex justify-between items-center">
          <div class="block">
            <h1 class="text-4xl font-semibold">{{ movies[curID].name }}</h1>
            <div class="flex border-t border-b border-gray-700 py-5 mt-5">
              <div>
                <h2 class="uppercase text-xl mb-3">Metascore</h2>
                <p class="w-3/5">
                  Universal acclaim based on 16 Critic Reviews
                </p>
              </div>
              <div class="flex items-center">
                <img
                  v-if="movies[curID].mustSee"
                  class="w-16 mx-3"
                  src="https://www.metacritic.com/images/icons/mc-mustsee.svg"
                  alt=""
                />
                <p
                  class="
                    mr-0
                    text-3xl
                    font-bold
                    px-1
                    py-3
                    bg-green-500
                    rounded-md
                  "
                >
                  {{ movies[curID].meta }}
                </p>
              </div>
            </div>
            <div
              class="
                flex
                justify-between
                items-start
                border-b border-gray-700
                py-5
              "
            >
              <div>
                <h2 class="uppercase text-xl mb-3">User Score</h2>
                <p class="w-3/5">
                  Universal acclaim based on 16 Critic Reviews
                </p>
              </div>
              <div class="flex items-center">
                <p
                  class="
                    mr-0
                    text-3xl
                    font-bold
                    px-1
                    py-3
                    bg-green-500
                    rounded-md
                  "
                >
                  {{ movies[curID].user }}
                </p>
              </div>
            </div>
          </div>
          <video muted autoplay :src="movies[curID].video"></video>
        </div>
      </div>
    </div>
    <div class="container mx-auto my-10">
      <div class="flex justify-between items-start">
        <div class="w-1/2 mr-5">
          <h2 class="text-2xl border-b border-gray-300 mb-5 pb-3">
            Critic Reviews
          </h2>
          <div class="border-b border-gray-300 py-6" v-for="critic of movies[curID].metacritic" :key="critic">
              <div class="flex items-center mb-3">
              <p class="mr-4 text-3xl font-bold bg-green-500 h-full p-3 rounded-md text-white">
                {{ critic.rate }}
              </p>
              <div>
                <img :src="critic.img" alt="" />
                <h3 class="font-bold">{{ critic.name }}</h3>
              </div>
            </div>
            <p>{{ critic.text }}</p>
          </div>
        </div>
        <div class="w-1/2 ml-5">
          <h2 class="text-2xl border-b border-gray-300 mb-5 pb-3">
            User Reviews
          </h2>
          <div class="border-b border-gray-300 py-6" v-for="critic of movies[curID].usercritic" :key="critic">
              <div class="flex items-center mb-3">
              <p class="mr-4 text-3xl font-bold bg-green-500 h-full p-3 rounded-md text-white">
                {{ critic.rate }}
              </p>
              <div>
                <h3 class="font-bold">{{ critic.name }}</h3>
                <p class="text-gray-300">{{ critic.date }}</p>
              </div>
            </div>
            <p>{{ critic.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      errors: [],
      movies: [],
      urlMovie: "http://localhost:3001/movies",
      movie: null,
      curID: this.$route.params.id - 1,
    };
  },
  async created() {
    try {
      const takeData = await fetch(this.urlMovie);
      const result = await takeData.json();
      this.movies.push(...result);
      console.log(this.movies);
    } catch (error) {
      this.errors.push(error);
    }
  },
  mounted() {
    const movie = this.movies.find(
      (movie) => movie.id == this.$route.params.id
    );
    if (movie) {
      this.movie = movie;
    }
  },
};
</script>