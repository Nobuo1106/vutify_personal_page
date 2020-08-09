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
        class="pa-5"
        cols="12"
        md="6"
      >
        <base-bubble-1 style="transform: translate(5%, -5%)" />

        <base-heading class="info--text">
          五十嵐伸雄とは
        </base-heading>

        <base-text class="mb-5">
          WEB、モバイルデベロッパーです。多言語のサイト制作からシステム開発まで請負います。
        </base-text>

        <base-subheading class="info--text">
          Skills
        </base-subheading>

        <base-text class="mb-5">
          言語：PHP, JavaScript, Objective-C, Swift<br>
          フレームワーク：CakePHP, Zend
        </base-text>

        <v-alert
          outlined
          color="info"
        >
          <v-row
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB;"
          >
            <v-col
              class="text-uppercase"
              cols="6"
              v-text="skill.name"
            />

            <v-col
              class="text-right"
              cols="6"
              v-text="`${skill.value}%`"
            />

            <v-progress-linear
              :value="skill.value"
              color="info"
              height="8"
            />
          </v-row>
        </v-alert>
      </v-col>

      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/aboutme.png')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    data: () => ({
      skills: [
        {
          name: 'PHP',
          value: 70,
        },
        {
          name: 'JavaScript',
          value: 70,
        },
        {
          name: 'Objective-C',
          value: 60,
        },
        {
          name: 'Swift',
          value: 60,
        },
      ],
    }),
  }
</script>
