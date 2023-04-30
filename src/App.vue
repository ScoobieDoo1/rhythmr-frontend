<template>
  <HeaderComp />
  <InstrumentCont />
  <FooterComp />
  
</template>

<script>
  import HeaderComp from './components/HeaderComp.vue';
  import FooterComp from './components/FooterComp.vue';
  import InstrumentCont from './components/InstrumentCont.vue';

export default {
  name: 'App',
  components: {
    HeaderComp,
    FooterComp,
InstrumentCont
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
