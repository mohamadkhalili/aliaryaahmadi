<template>
  <v-card>
    <v-row>
      <v-col
      cols="4"
      >
        <v-img/>
      </v-col>
      <v-col
      cols="8"
      >
        <v-card-title></v-card-title>
        <v-card-subtitle></v-card-subtitle>
        <v-card-text></v-card-text>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: "WorkCard",
  data() {
    return {
      work: null
    }
  }
}
</script>

<style scoped>

</style>
