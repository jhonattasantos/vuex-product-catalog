<template>
  <div>
      <a href="link.url"> {{link.name}} </a>
  </div>
</template>

<script>
export default {
  name: 'LinkAtom',
  props: {
    link: {
      required: true,
      type: Object
    }
  }
}
</script>

<style>

</style>
