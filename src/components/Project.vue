<template>
  <h1>This is a Vue component</h1>
  <h3>{{ name }}</h3>

  <ul>
    <li v-for="(item, index) in testList" :key="index">
      {{ item.title }}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Project',
  props: {
    name: String,
  },
  inject: ['testList']
}
</script>