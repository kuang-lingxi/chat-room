<template>
    <div>
        <div id="main">
            <Title />
            <!-- <input type="text"> -->
            <Main />
            <Input />
        </div>
    </div>
</template>

<script>
import Title from './Title';
import Input from './Input';
import Main from './Main';

export default {
    name: 'show',
    data() {
        return {

        }
    },
    components: {
        Title,
        Input,
        Main
    }
}
</script>

<style scope>
    #main {
        width:400px;
        height: 500px;
        border: 1px solid #ccc;
        border-radius: 10px;
        overflow: hidden;
    }
</style>
