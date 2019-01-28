<template>
  <div class="container">
    <div class="wrapper">
      <header-component></header-component>
      <Content></Content>
      <footer-component></footer-component>
    </div>
  </div>
</template>

<script>
  import Content from './content/Content';
  import HeaderComponent from './header/Header';
  import FooterComponent from './footer/Footer';

  export default {
    name: "index",
    components: {
      Content,
      HeaderComponent,
      FooterComponent,
    }
  }
</script>

<style scoped></style>
