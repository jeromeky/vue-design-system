<template>
  <button :class="['button ', variation]" v-on:click="onClick">
    <slot/>
  </button>
</template>

<script>
  export default {
    name: "LButton",
    status: "prototype",
    release: "0.0.1",
    props: {
      onClick: {
        type: String,
        required: false
      },
      variation: {
        type: String,
        default: "default",
        validator: value => {
          return value.match(/(default|disabled|strong|positive|negative)/)
        },
      },
    },
  }
</script>

<style lang="scss" scoped>
  .button {
    font-family: $font_family_text;
    background: $color_white;
    color: $color_oxford_blue;
    &.positive {
      background: $color_vermilion_darker;
      color: $color_oxford_blue;
    }
    &.negative {
      background: $color_vermilion_darker;
      color: $color_vermilion_light;
    }
  }
</style>

<docs>
  ```jsx
  <div>
    <l-button>Default</l-button>
    <l-button variation="positive">Save</l-button>
    <l-button variation="negative">Cancel</l-button>
  </div>
  ```
</docs>