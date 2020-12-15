<template>
  <popover
    name="tooltip"
    :pointer="pointer"
    :width="width"
    :event="event"
    @show="value = $event.value"
  >
    {{ $event.value.title }}
    {{ $event.value.artist }}
  </popover>
</template>
<script>
export default {
  name: 'Tooltip',
  props: {
    event: {
      type: String,
      default: 'hover'
    },
    pointer: {
      type: Boolean,
      default: false
    },
    width: {
      type: Number,
      default: 200
    }
  },
  data() {
    return {
      value: ''
    }
  }
}
</script>
