<script setup lang="ts">
import InventoryList from "@/components/inventory/InventoryList.vue";
import SideBar from "@/components/SideBarSkeleton.vue";
import Footer from "@/components/FooterSkeleton.vue";
</script>

<template>
    <main>
        <SideBar/>
        <InventoryList/>
        <Footer/>
    </main>
</template>

<style scoped lang="scss">
    main {
        max-width: 780px;
        margin: 0 auto;
        display: grid;
        grid-gap: 1.5rem;
        grid-template-columns: 236px max-content;
    }
</style>
