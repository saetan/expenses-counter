<template>
<div id="main-form">
    <form id="expenseForm">
        <p>
        <label for="name">Expense Name: </label>
        <input type="textarea" id="name" name="expenseForm">
        </p>
        <p>
        <label for="category">Category: </label>
        <select name="categories" id=category form="expenseForm" v-model="selected">
            <option v-for="option in options" :key="option.id" v-bind:value="option.value">
                {{ option.value}}
            </option>
            </select>
        </p>
        <p>
            <label for="amount">Amount: </label>
            <input type="number" id="amount" name="expenseForm">
        </p>
    </form>
</div>
</template>

<script>
export default {
    props: ['testing'],
    data(){ return {
        options: [{id: 1,value: "Groceries"}, {id: 2, value: "Bubble Tea"} ],
        selected: '',
        
    }} ,
    computed: {
        title() {
            return this.uwu + " " +this.testing
        }
    }
}
</script>
<style>
    body {
        background-color: #5CDB95;
    }

    #main-form {
        border: 1px solid black;
        background-color: #8EE4AF;
        display: inline-block;
        text-align: center;
    }

    form {
        display: inline-block;
        margin-left: auto;
        margin-right: auto;
        text-align: left;
        font-family: monospace;
        font-size:40px;
    }

    input {

        background-color: #8EE4AF;
        font-family: monospace;
        font-size:40px;
        outline:none;
    }

    select {
        font-size: 40px;
        font-family: monospace;
        background-color: #8EE4AF;
    }
</style>