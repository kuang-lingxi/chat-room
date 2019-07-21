<template>
    <div>
        <input id="input" type="text">
        <button class="btn"> Go </button>
        <!-- <textarea id="input" cols="30" rows="10"></textarea> -->
    </div>
</template>

<script>
export default {
    name: 'Input'
}
</script>

<style scoped>
    #input {
        width: 85%;
        height: 20px;
    }
    .btn {
        margin: 0;
        padding: 0;

        width: 10%;
    }
</style>
