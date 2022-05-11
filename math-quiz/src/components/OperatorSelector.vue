<template>
    <div>
    <button @click="$emit('changeOperator','+')">Addition (+)</button>
    <button @click="$emit('changeOperator','/')"> Devision (/)</button>
    <button  @click="$emit('changeOperator','-')">Subtraction(-)</button>
    <button @click="$emit('changeOperator','*')">Multiplication (*)</button>
    </div>
</template>
<script>
    export default {

    };


</script>
<style>

</style>