<template>
  <div class="checkbox-wrap" @click="handleClick($event)">
    <input type="checkbox" :value="value" :id="id" :checked="checked">
    <label :for="id">
      <i class="icon icon-checkbox-checked" v-if="checked"></i>
      <i class="icon icon-checkbox-unchecked" v-else></i>
      <slot></slot>
    </label>
  </div>
</template>

<script>
export default {
  name: 'vui-checkbox',
  props: {
    value: {
      type: String
    },
    id: {
      type: String
    },
    disabled: {
      type: Boolean,
      default: false
    },
    checked: {
      type: Boolean
    }
  },
  data: function() {
    return {
      value: {
        type: String
      },
      id: {
        type: String
      },
      disabled: {
        type: Boolean,
        default: false
      },
      checked: this.checked
    }
  },
  methods: {
    handleClick: function (eve) {
      this.checked = !this.checked
    }
  },
  computed: {
  }
}
</script>

<style scoped>
input[type="checkbox"]{
    display: none;
}
input[type="checkbox"]+label {
    display: inline-block;
    width: 48%;
    margin-top: 10px;
    margin-left: 5px;
    text-align: left;
    -webkit-box-sizing: border-box;
}
input[type="checkbox"]+label i {
  display: inline-block;
}
</style>
