<template>
  <section
    id="recent-projects"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col
        class="white text-center pa-5 info--text"
        cols="12"
        md="6"
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateX(25%)"
        />

        <base-heading>
          Professional<br>Career Status
        </base-heading>
        <br>
        <base-subheading>
          Job Title: R&D Coordinator<br>(Software Engineer)
        </base-subheading>
        <br>
        <base-subheading>
          Company: Alpha Aviation<br> Academy UAE
        </base-subheading>
        <br>
        <base-subheading>
          Skills
        </base-subheading>

        <v-row
          v-for="(skill, i) in skills"
          :key="i"
          align="center"
        >
          <v-col
            class="text-uppercase text-center"
            cols="7"
            v-text="skill.name"
          />
          <v-col
            class="text-right"
            cols="3"
          >
            <v-progress-circular
              :rotate="-90"
              :size="100"
              :width="15"
              :value="skill.level"
              color="secondary"
            >
              {{ skill.level }}%
            </v-progress-circular>
          </v-col>
        </v-row>
        <br>
        <br>
        <base-text class="mb-5">
          Driving License: Valid UAE driving license<br>
          Visa status: Resident Visa<br>
        </base-text>
      </v-col>

      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/alesia.jpeg')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'RecentProjects',

    data: () => ({
      skills: [
        {
          name: 'Web development',
          level: '75',
        },
        {
          name: 'Mobile app development',
          level: '89',
        },
        {
          name: 'Design',
          level: '63',
        },
        {
          name: 'Communication skills',
          level: '83',
        },
      ],
    }),
  }
</script>
