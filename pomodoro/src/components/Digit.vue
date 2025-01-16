<template>
  <svg
    class="digit"
    version="1.1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    x="0px"
    y="0px"
    width="366.5px"
    height="794px"
    viewBox="0 0 366.5 794"
    enable-background="new 0 0 366.5 794"
    xml:space="preserve"
  >
    <path
      :class="{ active: '02356789'.includes(data) }"
      class="digit-a"
      fill="#E60012"
      d="M359,14.5c0,8.008-6.492,14.5-14.5,14.5h-323C13.492,29,7,22.508,7,14.5l0,0C7,6.492,13.492,0,21.5,0h323
	C352.508,0,359,6.492,359,14.5L359,14.5z"
    />
    <path
      :class="{ active: '01234789'.includes(data) }"
      class="digit-b"
      fill="#E60012"
      d="M352,380c-8.008,0-14.5-6.492-14.5-14.5v-323c0-8.008,6.492-14.5,14.5-14.5l0,0
	c8.008,0,14.5,6.492,14.5,14.5v323C366.5,373.508,360.008,380,352,380L352,380z"
    />
    <path
      :class="{ active: '013456789'.includes(data) }"
      class="digit-c"
      fill="#E60012"
      d="M352,764c-8.008,0-14.5-6.492-14.5-14.5v-323c0-8.008,6.492-14.5,14.5-14.5l0,0
	c8.008,0,14.5,6.492,14.5,14.5v323C366.5,757.508,360.008,764,352,764L352,764z"
    />
    <path
      :class="{ active: '2345689'.includes(data) }"
      class="digit-d"
      fill="#E60012"
      d="M360,395.5c0,8.008-6.492,14.5-14.5,14.5h-323C14.492,410,8,403.508,8,395.5l0,0
	c0-8.008,6.492-14.5,14.5-14.5h323C353.508,381,360,387.492,360,395.5L360,395.5z"
    />
    <path
      :class="{ active: '0235689'.includes(data) }"
      class="digit-e"
      fill="#E60012"
      d="M359,779.5c0,8.008-6.492,14.5-14.5,14.5h-323C13.492,794,7,787.508,7,779.5l0,0
	c0-8.008,6.492-14.5,14.5-14.5h323C352.508,765,359,771.492,359,779.5L359,779.5z"
    />
    <path
      :class="{ active: '0456789'.includes(data) }"
      class="digit-f"
      fill="#E60012"
      d="M14.5,380c8.008,0,14.5-6.492,14.5-14.5v-323C29,34.492,22.508,28,14.5,28l0,0C6.492,28,0,34.492,0,42.5v323
	C0,373.508,6.492,380,14.5,380L14.5,380z"
    />
    <path
      :class="{ active: '0268'.includes(data) }"
      class="digit-g"
      fill="#E60012"
      d="M14.5,764c8.008,0,14.5-6.492,14.5-14.5v-323c0-8.008-6.492-14.5-14.5-14.5l0,0C6.492,412,0,418.492,0,426.5
	v323C0,757.508,6.492,764,14.5,764L14.5,764z"
    />
    <circle :class="{ active: data === ':' }" fill="#E60012" cx="207" cy="213.5" r="34.498" />
    <circle :class="{ active: data === ':' }" fill="#E60012" cx="207" cy="612.5" r="34.498" />
  </svg>
</template>

<script setup>
defineProps({
  data: {
    type: String,
    default() {
      return ''
    },
  },
  color: {
    type: String,
    default() {
      return 'white'
    },
  },
})
</script>

<style scoped lang="sass">
.digit
  width: 100px
  height: 297px
  margin: 7px

path, circle
  fill: transparent
  &.active
    // v-bind 把 CSS 的值和 Vue 的變數綁定
    fill: v-bind(color)
</style>
