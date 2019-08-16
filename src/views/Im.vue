<template>
    <div class="home">
        <img alt="Vue logo" src="../assets/logo.png">
        <div @click="showChat">sdfsf</div>
        <div v-model="this.text"></div>
    </div>
</template>

<script>
    import HelloWorld from '@/components/HelloWorld.vue'
    
    export default {
        name: 'im',
        data() {
            return {
                text: ''
            }
        },
        components: {
            HelloWorld
        },
        computed: {
            sessionlist() {
                let sessionlist = this.$store.state.sessionlist.filter(item => {
                    return item
                })
                return sessionlist
            }
        },
        methods: {
            showChat() {
                console.log(this.$store.state);
                console.log(this.$store.state.sessionlist);
                this.text = this.$store.state.sessionlist;
            }
        }
        
    }
</script>
