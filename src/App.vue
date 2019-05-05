<style lang="scss" scoped>
    #app {
        width: 680px;
        margin: 20px auto;
        font-family: Verdana, Sans-Serif; 

        h1 {
            color: #42b983;
            font-weight: bold;

        }

        textarea {
            display: block;
            width: 100%;
            min-height: 100px;
            padding: 0;
            margin: 20px 0;
            font-size: 16px;
        }
    }
</style>
<template>
    <div id="app">
        <h1>Just Enter Text:</h1>
        <textarea type="text" v-model="keyboardText"></textarea>
        <keyboard @sendText="getText"></keyboard>
    </div>
</template>

<script>
import Keyboard from './components/keyboard'

export default {
    data() {
        return {
            keyboardText:''
        }
    },

    components: {
        Keyboard
    },
    methods:{
        getText(msg){
            console.log(msg)
            this.keyboardText = msg
        }
    }
}
</script>