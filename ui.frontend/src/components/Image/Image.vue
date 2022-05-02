<template>
  <div class="error">
    <img :src="src" />
  </div>
</template>

<script>
export default {
  name: 'Image',
  props: {
    src: {
      type: String
    }
  }
}
</script>

<style scoped>
img {
  max-width: 40vw;
}

@media all and (max-width:404px) {
  img {
    max-width: 70vw;
  }
}

.error {
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>
