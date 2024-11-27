<script setup lang="ts">
import { ref } from 'vue';
import Table from './components/Table.vue';
import books from './bookdata';
import Card from './components/Card.vue';

const isTableView = ref(false);
</script>

<template>
  <button @click="isTableView = !isTableView" class="btn">
    {{ isTableView ? 'Card view' : 'Table view' }}
  </button>
  <Table v-if="isTableView" :books="books" />
  <Card v-else :books="books" />
</template>

<style scoped>
  .btn{
    background-color: blue;
    color: white;
    width: 100px;
    height: 40px;
    border-radius: 5px;
  }
</style>
