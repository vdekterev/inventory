<script setup lang="ts">
import BlurImage from '@/assets/skeleton-blur.png';
import ShimmerSkeleton from "@/components/ShimmerSkeleton.vue";
</script>

<template>
    <aside class="sidebar content-element">
        <img class="sidebar-image" :src="BlurImage" alt="skeleton blur" />
        <ShimmerSkeleton :amount="5"/>
    </aside>
</template>

<style scoped lang="scss">
    aside.sidebar {
        display: flex;
        flex-direction: column;
        gap: 20px;
        justify-content: center;
        padding: 18px 14px 24px;

        &-image {
            object-fit: contain;
            width: 208px;
            height: 240px;
        }
    }
</style>