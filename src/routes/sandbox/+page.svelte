<script lang="ts">
    import { Navbar } from '$lib/components/layout';
    import { Button, Header, MaterialSymbol, Deco } from '$lib/components';
    import { type MaterialSymbol as MaterialSymbolType } from 'material-symbols';
    import Footer from '$lib/components/layout/Footer.svelte';

    type Widget = [ MaterialSymbolType, string ];
    const widgets = [
        ['bolt', 'Boltageous'],
        ['token', 'Tokenomics'],
        ['browse_activity', 'Activity'],
        ['empty_dashboard', 'Carefully Engineered'],
        ['stacks', 'Stackflow'],
        ['globe', 'Decentralized'],
        ['workspace_premium', 'Award Winning'],
        ['diamond', 'High Endurance']
    ] as Widget[];

    const steps = [
        ['Select a Template', 'To help you get started quickly and easily, we offer a variety of pre-designed.'],
        ['Create Context', 'With our customizable dashboards, you can gain insights to into your.'],
        ['Browse Result', 'You can view your data as tables, charts or graphs, and you can drill down.'],
        ['Select a Template', 'To help you get started quickly and easily, we offer a variety of pre-designed.'],
        ['Create Context', 'With our customizable dashboards, you can gain insights to into your.']
    ] as const;
</script>

<div class="flex flex-col overflow-auto h-full items-center text-center">
    <Navbar />
    <Footer />
</div>

<style lang="scss">
    header {
        background: linear-gradient(1deg, #927EBC  0%,#FFFFFF  100%);
        background-clip: text;
        color: transparent;
    }
</style>