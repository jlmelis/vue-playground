<template>
  <input v-model="newItem" @keyup.enter="addItem" />
  <ItemList name="test project" />  
</template>

<script>
import ItemList from './ItemList'

export default {
  name: 'HelloWorld',
  data(){
    return ({
      newItem : '',
      testList: [
        {title: 'test 1' },
        {title: 'test 2' },
        {title: 'test 3' },
      ]
    })
  },
  methods: {
    addItem() {
      this.testList.push({title: this.newItem})
      console.log(this.testList)
    }
  },
  props: {
    msg: String
  },
  provide() {
    return {
      testList: this.testList,
    } 
  },
  components: {
    ItemList,
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
