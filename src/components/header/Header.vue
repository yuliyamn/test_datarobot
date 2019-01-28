<template>
  <div class="header">
    <a href="/" class="header-logo"><img class="header-logo__image" src="./assets/logo.png"></a>
    <p class="header-title">Real-Life Machine Learning. As Real as it Gets.</p>
  </div>
</template>

<script>
  export default {
    name: "Header"
  }
</script>

<style scoped lang="scss">
.header {
  border-bottom: 1px solid rgba(255,255,255,0.3);
  position: relative;
  height: 105px;
  padding-left: 200px;
  color: #fff;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;

  @media screen and (max-width: 600px) {
    padding-left: 0;
    padding-top: 55px;
    height: 80px;
  }

  &-logo {
    position: absolute;
    left: 0;
    top: 20px;
    padding: 13px 0;

    @media screen and (max-width: 600px) {
      left: 50%;
      margin-left: -93px;
      top: 6px;
    }

    &__image {
      height: 31px;
      width: 187px;
    }
  }

  &-title {
    font-size: 20px;
    line-height: 1.5em;
    text-align: right;
    max-width: 57%;

    @media screen and (max-width: 600px) {
      font-size: 15px;
      max-width: 80%;
      margin: 0 auto;
      text-align: center;
    }
  }
}
</style>
