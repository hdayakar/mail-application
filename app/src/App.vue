<template>
  <div id="app">
      <div class="container">
          <div class="mail-box">
                <app-sidebar :messages="messages"/>
                <app-content :messages="messages"/>
          </div>
      </div>
  </div>
</template>

<script>
    import Sidebar from "./components/Sidebar.vue";
    import Content from "./components/Content.vue";
    import messages from "./assets/data/messages";

    export default {
        data() {
            return {
                messages: messages
            };
        },
        name: "app",
        components: {
            appSidebar: Sidebar,
            appContent: Content
        }
    };
</script>

<style lang="scss">
    @import 'assets/style.css';
    @import '../node_modules/bootstrap/dist/css/bootstrap.min.css';
    @import '../node_modules/font-awesome/css/font-awesome.min.css';
</style>