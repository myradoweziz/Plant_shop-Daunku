<script setup>
import { defineProps } from 'vue'
import BaseIcon from '../BaseIcon.vue'
const props = defineProps({
  title: {
    type: String,
    default: () => ''
  },
  iconName: {
    type: String,
    default: () => ''
  },
  primaryBtn: {
    type: Boolean,
    default: () => false
  },
  pingColor: {
    type: Boolean,
    default: () => false
  },
  blueColor: {
    type: Boolean,
    default: () => false
  },
  radiusBtn: {
    type: String,
    default: () => ''
  },
  widthBtn: {
    type: String,
    default: () => ''
  },
  heightBtn: {
    type: String,
    default: () => ''
  }
})
</script>

<template>
  <button
    :style="`border-radius: ${props.radiusBtn}px; width: ${props.widthBtn}px; height: ${props.heightBtn}px`"
    :class="{ primary: props.primaryBtn, ping: props.pingColor, blue: props.blueColor }"
  >
    <p>
      {{ props.title }}
    </p>
    <BaseIcon :name="props.iconName" v-if="props.iconName" />
  </button>
</template>

<style lang="scss" scoped>
button {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  position: relative;
  cursor: pointer;
  padding: 12px 20px 12px 20px;
  font-family: 'Work Sans';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 26px;
  color: #101828;
  background-color: transparent;
  border: none;
  p {
    margin: 0;
    flex: 1 1 auto;
  }
  &.primary {
    color: #ffffff;
    background: #101828;
  }
  &.ping {
    padding: 0px 27px;
    color: #e29578;
    background-color: #fff3ea;
  }
  &.blue {
    color: #006d77;
    padding: 0px 10px;
    font-size: 12px;
    background-color: #bee1e6;
  }
}
</style>
