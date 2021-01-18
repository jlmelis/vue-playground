<template>
  <h1>This is a Vue component</h1>
  <h3>{{ name }}</h3>
</template>

<script>
export default {
  name: 'Project',
  props: {
    name: String,
  }
}
</script>