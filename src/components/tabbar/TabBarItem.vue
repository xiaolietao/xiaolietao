<template>
  <div id="tab-bar-item" @click="onClick">
    <div v-if="isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <slot name="item-text"></slot>
  </div>
</template>
<script>
export default {
  name: "TabBarItem",
  data:{
    isActive:true
  },
  methods: {
    onClick() {

    },
  },
};
</script>
<style>
#tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
#tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
  margin-bottom: 2px;
}
</style>