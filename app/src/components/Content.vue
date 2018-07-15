<template>
    <aside class="lg-side">
        <div class="inbox-head">
            <h3>{{ currentView.title }}</h3>
        </div>
        <keep-alive>
            <component :is="currentView.tag"></component>
        </keep-alive>
    </aside>
</template>

<script>
    // import inbox has a local component
    import Inbox from './Inbox.vue';

    export default {
        data() {
            return {
                history: [
                    {
                        tag: 'app-inbox',
                        title: 'Inbox'
                    }
                ]
            }
        },
        computed: {
            currentView() {
                return this.history[0];
            }
        },
        components: {
            appInbox: Inbox
        } 
    }
</script>
