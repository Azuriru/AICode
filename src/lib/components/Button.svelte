<script lang="ts">
    import type { MouseEventHandler } from 'svelte/elements';
    import { type MaterialSymbol } from 'material-symbols';
    import Icon from './MaterialSymbol.svelte';

    export let disabled = false;
    export let type: 0 | 1 | 2 = 1;
    export let thin = 0;
    export let width = '';
    export let bg = type ? 'bg-gradient-to-r from-purple-500 via-purple-400 to-purple-500' : '';
    export let size = 'text-sm';
    export let layout = '';
    export let icon: MaterialSymbol | undefined = undefined;
    export let onClick: MouseEventHandler<HTMLButtonElement> = () => {};

    let classes = `${width} ${bg} ${thin ? 'py-1 px-3' : 'py-2'} ${layout}  rounded-full ${size}`;
</script>

<button type="button" on:click={onClick} class="btn {classes}  " {disabled}>
    {#if icon}
        <Icon name={icon} />
    {/if}
    <slot />
</button>