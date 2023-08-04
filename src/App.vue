<template>
  OUTSIDE: {{ inputText }}
  <input type="text" v-model="inputText">
  <FormComponent v-model="inputText"></FormComponent>
  <SampleModel v-for="item in items" :key="item" v-model="inputText"></SampleModel>
</template>

<script>
import FormComponent from './components/FormComponent.vue'
import SampleModel from './components/SampleModel.vue'

export default {
  name: 'App',
  components: {
    FormComponent,
    SampleModel
  },
  data () {
    return {
      inputText: '',
      items: ['a', 'b', 'c']
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
