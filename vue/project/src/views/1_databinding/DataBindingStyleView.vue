<template>
  <div>
    <div style="color: red; font-size: 15px">
      스타일 바인딩: 글씨색은 red, 폰트크기는 15px
    </div>
    <div :style="style1">
      스타일 바인딩: 글씨색은 {{ style1.color }}, 폰트크기는
      {{ style1.fontSize }}
    </div>
    <button @click="style1.color = 'blue'">파란색으로 바꾸기</button>
    <button @click="style1.fontSize = '5px'">5px로 바꾸기</button>
    <br />
    <input type="number" v-model.number="style2.fontSizeNumber" />
    <select name="" id="" v-model="style2.color">
      <option value="black">검정</option>
      <option value="red">빨강</option>
      <option value="blue">파랑</option>
      <option value="green">초록</option>
    </select>
    <div :style="style2">
      스타일 바인딩: 글씨색은 {{ style2.color }}, 폰트크기는
      {{ style2.fontSize }}
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      style1: {
        color: 'green',
        fontSize: '25px'
      },
      style2: {
        color: 'black',
        fontSize: '22px',
        fontSizeNumber: 22
      }
    }
  },
  watch: {
    'style2.fontSizeNumber'(newValue) {
      const suffix = 'px'
      this.style2.fontSize = newValue.toString() + suffix
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeFont() {
      this.color = 'blue'
      this.fontSize = '22px'
    }
  }
}
</script>
