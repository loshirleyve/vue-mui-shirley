<template>
  <div>
    <vui-header fixed>Checkbox</vui-header>
    <page-content>
      <vui-checkbox v-model="checkboxValue.one" value="one">One</vui-checkbox>
      <vui-checkbox v-model="checkboxValue.two" value="two" disabled>Two (disabled)</vui-checkbox>
      <vui-checkbox v-model="checkboxValue.three" value="three" readonly>Two (readonly)</vui-checkbox>

    </page-content>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checkboxValue: {
        one: null,
        two: 'two',
        three: null
      }
    }
  }
}
</script>
