<script setup lang="ts">
import InventoryItem from "@/components/inventory/InventoryItem.vue";

const items = [
    { id: 1, name: "Item 1" },
    { id: 2, name: "Item 2" },
    { id: 3, name: "Item 3" },
    { id: 4, name: "Item 4" },
    { id: 5, name: "Item 5" },
    { id: 6, name: "Item 6" },
    { id: 7, name: "Item 7" }
];
const totalCells = 25;
</script>

<template>
    <div class="inventory-list content-element">
        <div v-for="cell in totalCells" :key="cell" class="inventory-list_cell">
            <InventoryItem v-if="items[cell - 1]" :id="items[cell - 1].id" />
        </div>
    </div>
</template>

<style scoped lang="scss">
    .inventory-list {
        display: grid;
        padding: 0;
        overflow: hidden;
        grid-template-columns: repeat(5, 1fr);
        grid-template-rows: repeat(5, 1fr);
        &_cell {
            width: 105px;
            height: 100px;
            outline: 0.5px solid var(--color-border);
        }
    }
</style>