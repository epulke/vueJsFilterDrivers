<template>
  <div class="image-box">
    <div class="image-text">
      <span>{{ msg }}</span>
    </div>
  </div>
</template>

<script>
import "./Image.scss"

export default {
  name: 'Image',
  props: {
    msg: String
  }
}
</script>