<template>
  <v-app style="background-color: #00000000 !important;">
    <v-row no-gutters class="ma-2 ma-sm-5 ma-md-5 ma-lg-10 ma-xl-10" >
      <v-container :style="'direction:' + this.$t('direction')">
        <v-col
          class="mt-5"
          cols="12"
          xs="12"
          sm="12"
          md="12"
          lg="12"
          xl="12"
        >
          <h3 style="text-align: center"><a class="text-decoration-none" style="color: #000" href="https://wa.me/+98-(921)2178078"> {{ Contacts[0].p1 }} : {{ Contacts[0].p2 }}  <v-icon size="30px" color="green">mdi-whatsapp</v-icon></a></h3>

        </v-col>
                <v-col
          class="mt-5"
          cols="12"
          xs="12"
          sm="12"
          md="12"
          lg="12"
          xl="12"
        >
          <h3 style="text-align: center">{{ Contacts[1].p1 }} : {{ Contacts[1].p2 }}</h3>
        </v-col>
                <v-col
          class="mt-5"
          cols="12"
          xs="12"
          sm="12"
          md="12"
          lg="12"
          xl="12"
        >

          <h3 style="text-align: center">{{ Contacts[2].p1 }} : {{ Contacts[2].p2 }}</h3>
        </v-col>
      </v-container>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "contact",
    data(){
    return {
      Contacts: [
        {
          p1: this.$t('Contact.p1.p1'),
          p2: this.$t('Contact.p1.p2'),
        },
        {
          p1: this.$t('Contact.p2.p1'),
          p2: this.$t('Contact.p2.p2'),
        },
        {
          p1: this.$t('Contact.p3.p1'),
          p2: this.$t('Contact.p3.p2'),
        },
      ]
    }
  }
}
</script>

<style scoped>

</style>
