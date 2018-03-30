<template>
  <div>
    <l-button variation="positive" :on-click="action">Save</l-button>
    <l-button variation="negative" :on-click="action">Cancel</l-button>
  </div>
</template>

<script>
  export default {
    name: "ActionButton",
    status: "prototype",
    release: "0.0.1",
    methods: {
      action: function() {
        alert('test');
      }
    }
  }
</script>

<style lang="scss" scoped>
</style>


<docs>
  ```jsx
  <div>
    <action-button/>
  </div>
  ```
</docs>