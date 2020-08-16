<template>
  <div>
    <v-btn
      v-for="(item, i) in items.slice(0, large ? items.length : 3)"
      :key="i"
      :href="item.link"
      fab
      target="_blank"
      class="ma-2"
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
<style scoped>
.ma-2 {
  position: relative;
  color: #e2e2ee;
  box-shadow: inset -1px -1px 2px rgba(0, 0, 0, 0.2),
              2px 2px 5px rgba(0, 0, 0, 0.2);
  transition: 0.3s;
}
.ma-2::before{
  background-color: rgba(0,0,255,1);
}
.v-size--default:hover {
  transform: translateY(-20px);
  box-shadow: inset -1ppx -1px 2px rgba(0, 0, 0, 0.2),
              2px 24px 10px rgba(0, 0, 0, 0.1);
}
.v-size--small:hover{
  transform: translateY(-10px);
  box-shadow: inset -1ppx -1px 2px rgba(0, 0, 0, 0.2),
              2px 24px 10px rgba(0, 0, 0, 0.1);
}
.v-size--default:before {
  content: '';
  position: absolute;
  top: 10px;
  left: 10px;
  right: 10px;
  bottom: 10px;
  border-radius: 50%;
  border: 10px solid rgb(0, 0, 0, 0.1);
}
.mdi-twitter{
  color: rgba(29, 161, 242) !important;
}
.fa-github{
  color:#24292e !important;
}
.mdi-facebook{
  color: rgba(24, 119, 242) !important;
}
.mdi-email{
  color: rgb(255, 195, 179) !important;
}
.mdi-phone{
  color: rgb(0, 118, 0) !important;
}

</style>
