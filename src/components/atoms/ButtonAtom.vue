<template>
  <div>
    <button class="btn"
            :style="{
                'background': (bg && !outline) ? bg : '',
                border: outline ? `1px solid green` : '' }"
            >
            {{label}}
    </button>
  </div>
</template>

<script>
export default {
  name: 'ButtonAtom',
  props: {
    label: {
      required: true,
      type: String
    },
    bg: {
      type: String
    },
    outline: {
      type: Boolean
    }
  }
}
</script>

<style>

.btn {
    padding: 10px 15px;
    margin: 10px;
    border: none;
}

.outline {
    border: 1px solid green;
}

</style>
