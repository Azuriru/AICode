<script lang="ts">
    export let layout = '';
</script>

<div class="deco flex items-center relative w-20 h-10 {layout}">
    <div class="trail w-full h-1" />
    <div class="star flex flex-shrink-0 w-3 h-3 rotate-45 rounded-sm absolute right-0" />
</div>

<style lang="scss">
    .deco {
        .trail {
            background: linear-gradient(to right, transparent, #927EBC);
        }

        .star {
            background: #927EBC;
        }
    }
</style>