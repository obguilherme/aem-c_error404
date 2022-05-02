<template>
  <div this-component-is-responsible-to-allow-custom-classes-on-aem></div>
</template>

<script>
export default {
  name: 'CustomClasses',
  mounted () {
    const containerLeft = document.querySelector('[cqpath="/content/vue/vue/jcr:content/root/responsivegrid/container_1794189691"] div')
    containerLeft.classList.add('central-content')

    const containerRight = document.querySelector('[cqpath="/content/vue/vue/jcr:content/root/responsivegrid/container"] div')
    containerRight.classList.add('central-content')
  }
}
</script>

<style lang="scss">
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  overflow-x: hidden;
  overflow-y: hidden;
}

.central-content {
  margin: 10% 0;
}
</style>
