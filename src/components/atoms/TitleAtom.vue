<template>
  <div>
      <component :is="tag"> {{content}} </component>
  </div>
</template>

<script>
export default {
  name: 'TitleAtom',
  props: {
    tag: {
      required: true,
      type: String
    },
    content: {
      required: true,
      type: String
    }
  }
}
</script>

<style>

</style>
