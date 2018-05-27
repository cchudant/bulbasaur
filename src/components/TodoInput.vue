<template>
  <form @submit.prevent="onSubmit">
    <span>Add new: </span>
    <input :value="value" @change="onChange">
    <input type="submit" value="Add">
  </form>
</template>

<script>
export default {
  name: 'TodoInput',
  data() {
    return {
      value: ''
    }
  },
  methods: {
    onChange(event) {
      this.value = event.target.value
    },
    onSubmit() {
      this.$emit('add', this.value)
      this.value = ''
    }
  }
}
</script>
