<template>
     <div>
        <input
          type="text"
          :value='value'
          class='search'
          placeholder="请输入内容"
          @input='ch'
      />

     </div>

</template>

<script>
export default {
  name: 'search',
  props: {
    value: {
      type: String,
      default: 'fy'
    }
  },
  methods: {
    ch (e) {
        this.$emit('input',e.target.value)
    }
  }
}
</script>

<style>
input{
  margin: 20px auto;
}
.search:after {
    content:''
}
</style>