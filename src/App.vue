<template>
  <h1 @click="increase">
    {{ count }}
  </h1>
  <div>
    4보다 큽니다!
  </div>
  <ul>
    <Fruit 
      v-for="fruit in fruits"
      :key="fruit"
      :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>

<script>
import Fruit from '~/components/Fruit'

export default {
  components: {
    // Fruit: Fruit, 이름이 같으면 생략이 가능하다
    Fruit
  },
  data() {
    return {
      // 반응성(Reactivity): 데이터를 갱신하면 화면도 바뀐다.
      count: 0,
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  methods: {
    increase() {
      this.count += 1;
    }
  }
}
</script>

<style lang="scss">
  h1 {
    font-size: 50px;
    color: royalblue;
  }
  ul{
    li {
      font-size: 40px;
    }
  }
</style>