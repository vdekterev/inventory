<script setup lang="ts">
defineProps({
    height: {
        type: String,
        default: '16px'
    },
    borderRadius: {
        type: String,
        default: '8px'
    },
    width: {
      type: String,
    },
    amount: {
        type: Number,
        default: 1
    },
    alignSelf: {
        type: String,
        default: 'center'
    }
});

const getRandomWidth = () => {
    return Math.floor(50 + Math.random() * 50) + '%';
}
</script>

<template>
    <div class="skeleton">
        <div class="skeleton-item" v-for="_ in amount" :style="{ height, borderRadius, alignSelf, width: width || getRandomWidth() }" />
    </div>
</template>

<style scoped lang="scss">

.skeleton {
    flex: 1 0 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1rem;

    &-item {
        background: linear-gradient(
                90deg,
                rgba(255, 255, 255, 0.1) 25%,
                rgba(255, 255, 255, 0.2) 50%,
                rgba(255, 255, 255, 0.1) 75%
        );
        background-size: 200% 100%;
        animation: shimmer 5s infinite;
    }
}

@keyframes shimmer {
    0% {
        background-position: -200% 0;
    }
    100% {
        background-position: 200% 0;
    }
}
</style>
