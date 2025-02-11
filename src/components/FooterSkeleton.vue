<script setup lang="ts">

import ShimmerSkeleton from "@/components/ShimmerSkeleton.vue";
</script>

<template>
    <footer class="content-element">
        <ShimmerSkeleton width="90%" height="36px" align-self="start" border-radius="12px"/>
        <span class="footer-close">&times;</span>
    </footer>
</template>

<style scoped lang="scss">
    footer {
        grid-column: span 2;
        display: flex;
        align-items: start;
        position: relative;
        .footer-close {
            position: absolute;
            top: 8px;
            right: 8px;
            height: 12px;
            width: 12px;
            padding: 8px;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-size: 1.5rem;
        }
    }
</style>