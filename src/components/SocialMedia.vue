<template>
  <div>
    <v-btn
      v-for="(item, i) in items.slice(0, large ? items.length : 3)"
      :key="i"
      :href="item.link"
      fab
      target="_blank"
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
          name: 'Twitter',
          icon: 'mdi-twitter',
          link: 'https://twitter.com/nobuoaida',
        },
        {
          name: 'Github',
          icon: 'fab fa-github',
          link: 'https://github.com/Nobuo1106',
        },
        {
          name: 'Facebook',
          icon: 'mdi-facebook',
          link: 'https://www.facebook.com/igarashi.nobuo',
        },
        {
          name: 'Email',
          icon: 'mdi-email',
          link: 'mailto:gonnbe1986@gmail.com',
        },
        {
          name: 'Phone',
          icon: 'mdi-phone',
          link: 'tel:08095204058',
        },
      ],
    }),
  }
</script>
