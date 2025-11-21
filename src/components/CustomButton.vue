<script setup lang="ts">
defineProps<{
    label: string;
    click?: () => void;
    secondary?: boolean;
    redFontColor?: boolean;
}>();
</script>

<template>
    <button :class="{ 'btn-secondary': secondary, 'red-font-color': redFontColor }" class="poppins-medium">{{ label }}</button>
</template>

<style scoped>
button {
    width: 100%;
    height: 45px;

    background-color: var(--primary-color);
    color: var(--font-button-primary);
    border-radius: 16px;
    border: none;
    transition: 0.5s;
}

button:hover {
    transition: 0.5s;
    cursor: pointer;
    background-color: var(--button-hover);
}

.btn-secondary {
    background-color: var(--button-secondary);
    color: var(--font-color);
    border: 1px solid;
    border-color: var(--input-border-color);
}

.btn-secondary:hover {
    background-color: var(--button-primary);
    color: var(--font-button-primary);
}

.red-font-color {
    color: var(--primary-color);
}
</style>

