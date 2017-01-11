<template>
  <div>
    <input type="checkbox" id="checkbox_a" class="chk_1">
    <label for="checkbox_a">check<i class="icon icon-checkbox-unchecked"></i></label>

    
  </div>
</template>

<script>
export default {
  name: 'vui-checkbox',
  data: function() {
    return {
      icons: ['checkbox-unchecked', 'checkbox-checked', 'checkbox-checked-fill']
    }
  }
}
</script>

<style scoped>
.chk_1 {
  display: none;
}
.chk_1 + label:before {
  content: '\e720';
  display: inline-block;
  position: relative;
}
.chk_1:active + label:before {
  content: '\e721';
  display: inline-block;
  position: relative;
}
.chk_1:checked + label:before {
  content: '\e722';
  display: inline-block;
  position: relative;
}
</style>
