<template>
  <v-card>
    <v-card-title>hello</v-card-title>
    <v-card-text>
      <v-textarea v-model="txt" />
    </v-card-text>
    <v-card-actions>
      <v-btn @click="test">test</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      txt: '',
    }
  },
  methods: {
    async test() {
      const r = await this.$axios.get('/api')
      this.txt = r.data
    },
  },
}
</script>
