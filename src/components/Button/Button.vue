<template>
  <button class="button">{{ msg }}</button>
</template>

<script>
import "./Button.scss"

export default {
  name: 'Button',
  props: {
    msg: String
  }
}
</script>