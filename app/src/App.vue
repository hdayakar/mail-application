<template>
  <div id="app">
      <div class="container">
          <div class="mail-box">
                <Sidebar/>
          </div>
      </div>
  </div>
</template>

<script>
    import Sidebar from "./components/Sidebar.vue";

    export default {
        name: "app",
        components: {
            Sidebar
        }
    };
</script>

<style lang="scss">
    @import 'assets/style.css';
    @import '../node_modules/bootstrap/dist/css/bootstrap.min.css';
    @import '../node_modules/font-awesome/css/font-awesome.min.css';
</style>