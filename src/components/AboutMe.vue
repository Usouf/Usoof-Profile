<template>
  <section
    id="about"
    class="overflow-hidden"
  >
    <v-row
      class="white"
      no-gutters
    >
      <v-col
        class="pl-10"
        cols="12"
        md="6"
      >
        <base-bubble-1 style="transform: translate(5%, -5%)" />

        <base-heading class="info--text">
          About Me
        </base-heading>
        <br>
        <base-subheading class="info--text">
          Bio
        </base-subheading>
        <base-text class="mb-5">
          Birthday: 19 April 1996<br>
          Nationality: Indian<br>
          Height: 5' 10" (178cm)<br>
          Religion: Islam<br>
        </base-text>

        <base-subheading class="info--text">
          Hobbies
        </base-subheading>

        <v-row
          v-for="(hobby, i) in Hobbies"
          :key="i"
        >
          <v-col
            cols="6"
            v-text="hobby.name"
          />
        </v-row>

        <base-subheading class="info--text">
          Languages
        </base-subheading>

        <v-row
          v-for="(lang, i) in Languages"
          :key="i"
        >
          <v-col
            class="text-uppercase"
            cols="6"
            v-text="lang.name"
          />
          <v-col
            class="text-right"
            cols="2"
            v-text="lang.level"
          />
        </v-row>
      </v-col>

      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/guille.jpeg')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'AboutMe',
    data: () => ({
      Languages: [
        {
          name: 'Arabic',
          level: 'Native',
        },
        {
          name: 'Urdu',
          level: 'Native',
        },
        {
          name: 'English',
          level: 'Professional',
        },
      ],
      Hobbies: [
        {
          name: 'Coding',
        },
        {
          name: 'Table Tennis',
        },
        {
          name: 'Volleyball',
        },
      ],
    }),

  }
</script>
