<template>
    <div id="app">
        <div id="nav">
            <router-link to="/">Home</router-link>
            |
            <router-link to="/about">About</router-link>
            |
            <router-link to="/im">Im聊天页面</router-link>
        </div>
        <router-view/>
    </div>
</template>

<script>
    
    export default {
        data() {
            return {}
        },
        // 所有页面更新都会触发此函数
        created() {
            // 提交sdk连接请求
            this.$store.dispatch('connect');
            // this.$store.dispatch('updateRefreshState')
        },
    }

</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }
    
    #nav {
        padding: 30px;
    }
    
    #nav a {
        font-weight: bold;
        color: #2c3e50;
    }
    
    #nav a.router-link-exact-active {
        color: #42b983;
    }
</style>
