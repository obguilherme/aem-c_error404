<template>
  <header>
    <p>404 NOT FOUND</p>
  </header>
</template>

<script>
// Imports

export default {
  name: 'Header'
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@700&display=swap');

header {

display: flex;
flex-direction: row;

left: 77px;
top: 40px;

font-family: 'Inconsolata', monospace;
font-style: normal;
font-weight: 700;
font-size: 24px;
line-height: 25px;
letter-spacing: -0.08em;
text-transform: uppercase;

color: #333333;
}
</style>
