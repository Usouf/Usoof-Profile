<template>
  <section
    id="get-in-touch"
    class="overflow-hidden"
  >
    <v-row
      align="center"
      justify="center"
      class="accent info--text"
      no-gutters
    >
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/florian.jpeg')"
          height="100%"
        />
      </v-col>

      <v-col
        class="text-center"
        cols="12"
        md="6"
      >
        <base-bubble-1 />

        <base-heading class="ma-5 mb-5">
          Get In Touch
        </base-heading>
        <v-sheet
          color="pl-10 pr-10 transparent"
        >
          <v-text-field
            class="centered-input"
            color="info"
            label="Phone"
            outlined
            flat
            disabled
            value="0563858825"
            prepend-inner-icon="mdi-phone"
          />

          <v-text-field
            class="centered-input"
            color="info"
            label="Email"
            outlined
            flat
            disabled
            value="yousuf.m.n@gmail.com"
            prepend-inner-icon="mdi-email"
          />
        </v-sheet>
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'GetInTouch',
  }
</script>

<style scoped>
    .centered-input >>> input {
      text-align: center
    }
    .toggle.v-input--is-disabled.v-text-field .v-input{
      border-color: #fff;
    }
</style>
