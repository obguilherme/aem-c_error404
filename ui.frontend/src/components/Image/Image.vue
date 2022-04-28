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

@media all and (max-width: 360px) {
  .error {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
.error {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
}

</style>
