<template>
  <div>
    <input type="text" name="" id="" v-bind:value="userId" readonly />
    <input type="text" name="" id="" :value="userId" readonly />
    <br>
    <br>
    <img :src="imgSrc" alt="" style="width:100px; height:auto;">
    <br>
    <br>
    <input type="search" name="" id="" v-model="txt1" />
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'aaa',
      imgSrc: 'https://aoroa.ai/wp-content/uploads/2021/07/cropped-cropped-Asset-1-2.png',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
