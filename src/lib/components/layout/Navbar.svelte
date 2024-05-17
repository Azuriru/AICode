<script lang="ts">
    import MaterialSymbol from '../MaterialSymbol.svelte';

    const navOptions = [
        'Home',
        'Litepaper',
        'About'
    ] as const;
</script>

<div class="navbar z-10 max-w-7xl flex items-center justify-between w-full pb-8 px-8 md:px-16 flex-grow-0 sticky top-0 pt-8 mx-auto max-md:backdrop-blur">
    <div class="logo">
        <img src="/logo.svg" alt="logo" />
    </div>
    <div class="nav-items hidden md:flex bg-white/10 rounded-full backdrop-filter backdrop-blur">
        {#each navOptions as option (option)}
            <div class="nav-option flex py-4 px-6 opacity-50 hover:opacity-100">
                {option}
            </div>
        {/each}
    </div>
    <div class="join-hub hidden md:flex font-semibold">
        Join hub
    </div>
    <div class="menu flex items-center md:hidden gap-4">
        <button type="button" class="flex text-2xl ">
            <MaterialSymbol name="menu" />
        </button>
        Menu
    </div>
</div>

<style lang="scss">
</style>