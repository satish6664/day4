<template>
    <div v-if="ShowBooks">
        <h2>{{ title }}</h2>
        <p> {{ price }}</p>
    </div>
    <div v-else>No Books</div>

    <button @click="ToggleShowBooks">
        <span v-if="ShowBooks">Hide Books</span>
        <span v-else>Show Books</span>
    </button>
</template>
<script setup>

import { ref } from 'vue';
    const ShowBooks=ref(true)
    const title=ref("The Book")
    const price=ref(40)

    function ToggleShowBooks()
    {
        ShowBooks.value=!ShowBooks.value
    }
</script>