<template>
  <div id="app" class="container">
    <app-header></app-header>
    <hr>
    <app-server-list></app-server-list>
    <hr>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './components/Shared/Header'
import Footer from './components/Shared/Footer'
import ServerList from './components/Server/ServerList'

export default {
  name: "app",
  components: {
    'app-header': Header,
    'app-footer': Footer,
    'app-server-list': ServerList,
  }
};
</script>

<style>

</style>
