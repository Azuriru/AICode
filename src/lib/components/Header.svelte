<script lang="ts">
    import Deco from './Deco.svelte';

    export let deco = true;
    export let layout = 'max-w-2xl items-center text-5xl font-semibold mx-auto';
</script>

<header class="header flex flex-col gap-4 {layout}">
    {#if deco}
        <Deco />
    {/if}
    <slot />
</header>

<style lang="scss">
    header {
        background: linear-gradient(90deg, #8D65E9  0%,#5391E4  47.61904761904761%,#6BCD94  100%);
        background-clip: text;
        color: transparent;
    }
</style>