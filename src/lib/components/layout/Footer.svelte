<script lang="ts">
    import MaterialSymbol from '../MaterialSymbol.svelte';

    const footerOptions = [
        'Management',
        'Reporting',
        'Tracking',
        'Subscribe',
        'Company'
    ] as const;
</script>

<div class="footer z-10 max-w-7xl flex flex-col items-center w-full px-8 md:px-16 flex-grow-0 mx-auto pt-16 gap-16">
    <div class="d-vider flex h-[1px] w-full bg-gradient-to-r from-transparent via-[#927EBC] to-transparent" />
    <div class="logo">
        <img src="/logo.svg" alt="logo" />
    </div>
    <div class="footer-options flex flex-wrap gap-8 justify-evenly *:opacity-50 hover:*:opacity-100 *:transition-opacity">
        {#each footerOptions as option (option)}
            <div class="footer-option flex">
                {option}
            </div>
        {/each}
    </div>
    <div class="socials flex items-center text-3xl gap-8 *:opacity-50 hover:*:opacity-100 *:transition-opacity">
        <MaterialSymbol name="api" />
        <MaterialSymbol name="api" />
        <MaterialSymbol name="api" />
    </div>
</div>

<style lang="scss">
</style>