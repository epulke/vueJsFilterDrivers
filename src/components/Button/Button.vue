<template>
  <button class="button" @click="onClick">{{ msg }}</button>
</template>

<script>
import "./Button.scss"

export default {
  name: 'Button',
  props: {
    msg: String,
    onClick: Function,
  }
}
</script>