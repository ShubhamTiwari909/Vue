<template>
  <div>
    <div class="grid grid-cols-1 lg:grid-cols-4 md:grid-cols-3">
      <h1 v-for="movie in movies" :key="movie">
        {{ movie }}
      </h1>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-4 md:grid-cols-3">
      <h1 v-for="movie in movies" :key="movie">
       <p v-if="movie === 'Spiderman' || movie === 'Avengers'"> {{ movie }}</p>
      </h1>
    </div>

    <div
      class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-2 my-10 py-5 bg-slate-800 text-indigo-200 text-center"
    >
      <div
        v-for="fields in field"
        :key="fields.name"
        class="border-x-2 px-2 my-4 border-red-300"
      >
        <h1 class="my-20 text-3xl">
          {{ fields.name }}
        </h1>
        <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-2">
          <p
            class="py-5 mx-3 my-5 bg-indigo-500 rounded-md"
            v-for="language in fields.Languages"
            :key="language"
          >
            {{ language }}
          </p>
        </div>
      </div>
    </div>
   
  </div>
</template>

<script>
export default {
  name: "Loops",
  data() {
    return {
      movies: ["Avengers", "Spiderman", "Dr. Strange", "Batman"],
      field: [
        {
          name: "Android",
          Languages: ["Java", "Kotlin", "Flutter", "React Native"],
        },
        {
          name: "Web Development",
          Languages: ["HTML", "CSS", "JAVASCRIPT", "TAILWIND", "React"],
        },
        {
          name: "Backend",
          Languages: ["MySQL", "MongoDB", "PostgreSQL", "Cassanndra"],
        },
      ],
    };
  },
  methods: {},
};
</script>

<style></style>
