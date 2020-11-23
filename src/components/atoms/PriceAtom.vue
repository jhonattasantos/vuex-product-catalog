<template>
  <div>
    <p> {{content}} </p>
  </div>
</template>

<script>
export default {
  name: 'PriceAtom',
  props: {
    content: {
      required: true,
      type: String
    }
  }
}
</script>

<style scoped>
  p {
    font-weight: bold;
  }
</style>
