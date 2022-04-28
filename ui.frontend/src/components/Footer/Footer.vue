<template>
  <div class="foot">
    <footer >
      <p>created by <b>guilherme.bechel</b> - devChallenges.io</p>
    </footer>
  </div>
</template>

<script>
// Imports

export default {
  name: 'Footer'
}
</script>

<style >
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500;700&display=swap');

.foot {
  display: flex;
  flex-direction: column;
  align-items: center;

  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;

  color: #BDBDBD;
}
</style>
