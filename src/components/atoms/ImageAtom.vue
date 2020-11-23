<template>
  <div>
      <img :src="path" />
  </div>
</template>

<script>
export default {
  name: 'ImageAtom',
  props: {
    path: {
      required: true,
      type: String
    }
  }
}
</script>

<style>

</style>
