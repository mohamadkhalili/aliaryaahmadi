<template>
  <v-container>
    <h1 class="ma-2" :style="style_title">{{ $t('Biography.p_public.title') }}</h1>
    <h2 class="ma-4" :style="style_subtitle">{{ $t('Biography.p_public.subtitle') }}</h2>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.p_public.p1') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.p_public.p2') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.p_public.p3') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.p_public.p4') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.p_public.p5') }}</h3>
    <h2 class="ma-4" :style="style_subtitle">{{ $t('Biography.music_live.subtitle') }}</h2>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p1') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p2') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p3') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p4') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p5') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p6') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p7') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p8') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p9') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.music_live.p10') }}</h3>
    <h2 class="ma-4" :style="style_subtitle">{{ $t('Biography.c_music.subtitle') }}</h2>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p1') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p2') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p3') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p4') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p5') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p6') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.c_music.p7') }}</h3>
    <h2 class="ma-4" :style="style_subtitle">{{ $t('Biography.tech_music.subtitle') }}</h2>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.tech_music.p1') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.tech_music.p2') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.tech_music.p3') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.tech_music.p4') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.tech_music.p5') }}</h3>
    <h2 class="ma-4" :style="style_subtitle">{{ $t('Biography.edit_music.subtitle') }}</h2>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.edit_music.p1') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.edit_music.p2') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.edit_music.p3') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.edit_music.p4') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.edit_music.p5') }}</h3>
    <h2 class="ma-4" :style="style_subtitle">{{ $t('Biography.actives.subtitle') }}</h2>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.actives.p1') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.actives.p2') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.actives.p3') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.actives.p4') }}</h3>
    <h3 class="ma-4" :style="style_p">{{ $t('Biography.actives.p5') }}</h3>
  </v-container>
</template>

<script>
export default {
  name: "bio",
  data() {
    return {
      style_title: "direction:" + this.$t('direction') + ";line-height: 3;",
      style_subtitle: "direction:" + this.$t('direction') + ";line-height: 2.3;",
      style_p: "direction:" + this.$t('direction') + ";line-height: 2;"
    }
  }
}
</script>

<style scoped>

</style>
