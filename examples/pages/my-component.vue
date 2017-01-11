<template>
  <div>
    <vui-header fixed>my-component</vui-header>
    <page-content>
      <my-component></my-component>
    </page-content>
  </div>
</template>

<script>
var Child = {
  template: '<div>a custom component!</div>'
}
export default {
  components: {
    'my-component': Child
  }
}
</script>
