<template>
  <div>
    <div>
      <select name="" id="">
        <option value=""></option>
        <option :value="city.code" :key="city.code" v-for="city in cities">
          {{ city.title }}
        </option>
      </select>
    </div>
    <table>
      <thead>
        <tr>
          <th>제품번호</th>
          <th>제품명</th>
          <th>가격</th>
          <th>주문수량</th>
          <th>합계</th>
        </tr>
      </thead>
      <tbody>
        <tr :key="i" v-for="(drink, i) in drinkList">
          <td>{{ drink.drinkId }}</td>
          <td>{{ drink.drinkName }}</td>
          <td>{{ drink.price }}</td>
          <td><input type="number" name="" id="" v-model="drink.qty" /></td>
          <td>{{ drink.price * drink.qty }}</td>
        </tr>
        <!-- <tr :key="drink.drinkId" v-for="drink in drinkList"></tr> -->
      </tbody>
    </table>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '063' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: '코카콜라1',
          price: 100,
          qty: 1
        },
        {
          drinkId: '2',
          drinkName: '코카콜라2',
          price: 200,
          qty: 2
        },
        {
          drinkId: '3',
          drinkName: '코카콜라3',
          price: 300,
          qty: 3
        },
        {
          drinkId: '4',
          drinkName: '코카콜라4',
          price: 400,
          qty: 4
        }
      ]
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
