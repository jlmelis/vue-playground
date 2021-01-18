<template>
  <Project name="test project" />
</template>

<script>
import Project from './Project'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  provide: {
    testList: [
      {title: 'test 1' },
      {title: 'test 2' },
      {title: 'test 3' },
    ]
  },
  components: {
    Project,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
