<template>
  <div>
    <v-btn
      v-for="(item, i) in items.slice(0, large ? items.length : 2)"
      :key="i"
      fab
      :href="item.href"
      class="ma-2"
      color="info"
      :small="!large"
    >
      <v-icon
        dark
        v-text="item.icon"
      />
    </v-btn>
  </div>
</template>

<script>
  export default {
    props: {
      large: {
        type: Boolean,
        default: false,
      },
    },

    data: () => ({
      items: [
        {
          name: 'Instagram',
          icon: 'mdi-instagram',
          href: 'https://www.instagram.com/yousufmansoor/',
        },
        {
          name: 'LinkedIn',
          icon: 'mdi-linkedin',
          href: 'https://www.linkedin.com/in/usoof-mansoor/',
        },
      ],
    }),
  }
</script>
