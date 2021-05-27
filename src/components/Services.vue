<template>
  <section
    id="services"
    class="overflow-hidden"
  >
    <v-row
      class="accent"
      no-gutters
    >
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/aboutme.png')"
          height="100%"
        />
      </v-col>

      <v-col
        class="text-center pa-5"
        cols="12"
        md="6"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <v-col cols="12">
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="info--text">
              Educational<br>Qualifications
            </base-heading>
          </v-col>

          <v-col
            v-for="(service, i) in services"
            :key="i"
            class="text-center mb-3"
            md="6"
          >
            <v-avatar
              class="elevation-6 mb-2"
              color="#BFADA5"
              size="64"
              tile
            >
              <v-icon
                dark
                size="52"
                v-text="service.icon"
              />
            </v-avatar>

            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.blurb" />
            </base-text>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'Education',

    data: () => ({
      services: [
        {
          name: 'Hafiz Quran',
          icon: 'mdi-book-open-page-variant',
          blurb: 'Markaz Mohammed Bin Salem Bakheet',
        },
        {
          name: 'High School',
          icon: 'mdi-school',
          blurb: 'Islamic School for training and education',
        },
        {
          name: 'BSc. Computer Engineer',
          icon: 'mdi-laptop',
          blurb: 'Ajman University',
        },
        {
          name: 'Mobile & Web Development',
          icon: 'mdi-android',
          blurb: 'Online',
        },
      ],
    }),
  }
</script>
