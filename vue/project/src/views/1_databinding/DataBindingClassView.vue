<template>
  <div>
    <div :class="{ active: isActive, 'text-red': hasError }">클래스 바인딩</div>
    <div :class="class2">클래스 바인딩2</div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      hasError: false,
      class2: ['active', 'text-red']
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
<style scoped>
.active {
  /* 클래스 명이 -, _, . 등으로 구분되어 있지 않으면, 클래스에서 지정해줄 때 따옴표로 묶을 필요 없다. */
  background-color: greenyellow;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
