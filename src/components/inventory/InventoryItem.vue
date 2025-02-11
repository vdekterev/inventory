<script setup lang="ts">
defineProps({
    id: Number,
    amount: Number,
    backgroundColor: {
        type: String,
        default: '#B8D998'
    },
})
</script>

<template>
    <div class="inventory-item">
        <div class="inventory-item_image">
            <div :style={backgroundColor}></div>
            <div :style={backgroundColor}></div>
        </div>
        <div class="inventory-item_amount">2</div>
    </div>
</template>

<style scoped lang="scss">
    .inventory-item {
        padding: 23px;
        height: 100%;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        &_image {
            div {
                width: 48px;
                height: 48px;
                position: absolute;
                top: 0;
                left: 0;
                transform: translate(70%, 60%);
                &:nth-child(1) {
                    top: -10px;
                    left: -10px;
                    backdrop-filter: blur(12px);
                }
                &:nth-child(2) {}
            }
        }
        &_amount {
            font-size: 10px;
            width: 16px;
            height: 16px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-width: 1px 0 0 1px;
            border-style: solid;
            border-color: var(--color-border);
            border-top-left-radius: 6px;
            position: absolute;
            bottom: 0;
            right: 0;
            color: rgba(242, 242, 242, 0.4);
        }
    }
</style>