<template>
  <div>
    <p> {{content}} </p>
  </div>
</template>

<script>
export default {
  name: 'SimpleTextAtom',
  props: {
    content: {
      required: true,
      type: String
    }
  }
}
</script>

<style>

</style>
