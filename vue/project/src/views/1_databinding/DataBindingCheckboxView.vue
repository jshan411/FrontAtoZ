<template>
  <div>
    <div>
        <input type="checkbox" name="" id="html" value="HTML" v-model="favoriateLanguage" />
        <label for="html">HTML</label>
    </div>
    <div>
        <input type="checkbox" name="" id="css" value="CSS" v-model="favoriateLanguage" />
        <label for="css">CSS</label>
    </div>
    <div>
        <input type="checkbox" name="" id="js" value="JS" v-model="favoriateLanguage" />
        <label for="js">JS</label>
    </div>
    <div>선택한 언어: {{ favoriateLanguage }}</div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      favoriateLanguage: ['JS']
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
