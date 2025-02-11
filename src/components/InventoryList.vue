<script setup lang="ts">

</script>

<template>
    <div id="inventory-list" class="content-element">
        тут будут inventory-list__item
    </div>
</template>

<style scoped lang="scss">
    #inventory-list {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-template-rows: repeat(5, 1fr);
    }
</style>