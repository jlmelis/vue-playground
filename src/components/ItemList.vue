<template>
  <h3>{{ name }}</h3>

  <ul>
    <li v-for="(item, index) in testList" :key="index">
      {{ item.title }}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ItemList',
  props: {
    name: String,
  },
  inject: ['testList']
}
</script>