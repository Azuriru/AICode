<script lang="ts">
    import { Footer, Navbar } from '$lib/components/layout';
    import { Button, Header, MaterialSymbol, Deco } from '$lib/components';
    import { type MaterialSymbol as MaterialSymbolType } from 'material-symbols';

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

    const gateway = ['Social Protocol', 'Community', 'Consensus Aggregation', 'Connection', 'Token Allocation'];
    const gateway2 = ['Chat', 'Link', 'Bridge', 'Explore', 'Thrive'];

    const devs = ['Rewarding Transition: Empowering Web2 Communities for Web3 Success', 'Quantitative Value: Driving Community Growth Through Engagement', 'Active Engagement: Fostering Community Growth and Rewards', 'Project Prosperity: Linking Quality Projects to Premium Communities'];

    const devsdesc = ['Rewarding Transition: Empowering Web2 Communities for Web3 Success', 'Quantitative Value: Driving Community Growth Through Engagement', 'Active Engagement: Fostering Community Growth and Rewards', 'Project Prosperity: Linking Quality Projects to Premium Communities'];
</script>

<div class="flex flex-col overflow-auto h-full items-center text-center">
    <Navbar />
    <!-- if zk changes his mind and says it looks so weird cause its too wide, put this back: md:max-w-7xl -->
    <div class="main flex flex-col items-center h-full w-full max-w-full gap-20 [&>div:last-of-type]:pb-20">
        <!-- One -->
        <div class="info flex flex-col flex-shrink-0 justify-center items-center gap-12  h-4/5">
            <Header deco={false} layout="items-center text-5xl md:text-5xl font-semibold whitespace-pre-line">
                Discover Connections, Embrace Growth, Thrive in Unity
            </Header>
            <span class="description text-xl font-semibold px-8 max-w-6xl text-slate-300">Join us on a journey where connection fuels exploration, and together, we thrive in a community bound by shared discovery and growth.</span>
            <Button>Join Now</Button>
        </div>
        <!-- Two & Three -->
        <div class="tools flex flex-col flex-shrink-0 min-h-full w-full gap-28">
            <div class="marquee flex flex-wrap justify-center w-full overflow-hidden flex-shrink-0 text-sm gap-4 *:w-64">
                <div class="item flex flex-col items-center justify-center p-4 gap-3 rounded bg-white/10">
                    <div class="text-4xl font-semibold">4000+</div>
                    <div class="text-slate-300">Onboarded Community</div>
                </div>
                <div class="item flex flex-col items-center justify-center p-4 gap-3 rounded bg-white/10">
                    <div class="text-4xl font-semibold">1,000,000</div>
                    <div class="text-slate-300">Community Members</div>
                </div>
                <div class="item flex flex-col items-center justify-center p-4 gap-3 rounded bg-white/10">
                    <div class="text-4xl font-semibold">5,000,000</div>
                    <div class="text-slate-300">Daily Conversation</div>
                </div>
                <div class="item flex flex-col items-center justify-center p-4 gap-3 rounded bg-white/10">
                    <div class="text-4xl font-semibold">25+</div>
                    <div class="text-slate-300">Associated Project</div>
                </div>
            </div>
            <div class="dev-tools flex max-lg:flex-col max-lg:gap-12 xl:gap-20 justify-center">
                <div class="header flex flex-col gap-8 lg:w-96 lg:text-left">
                    <Header layout="items-center lg:items-start text-5xl font-semibold">Connect with Tendopia</Header>
                    <span class="description text-xl font-medium max-lg:px-8">Discover revolutionary social protocols for effortless consensus building and embark on an exciting journey into the digital future with us.</span>
                </div>
                <div class="cards flex max-sm:flex-col max-sm:w-full text-xl items-center justify-center gap-4 sm:gap-6 max-sm:px-4 lg:mt-40">
                    <div class="flex flex-col w-full sm:items-end sm:w-80 gap-4">
                        <div class="news card p-8 flex flex-col justify-center items-center gap-4 sm:w-2/3">
                            <MaterialSymbol name="news" size={40} />
                            Consensus Aggregation
                        </div>
                        <div class="generation card p-8 flex flex-col justify-center items-center gap-4 w-full sm:h-40">
                            <MaterialSymbol name="edit" size={40} />
                            Fair Distribution Protocol
                        </div>
                    </div>
                    <div class="generation card p-8 flex flex-col justify-center items-center gap-4 max-sm:w-full sm:h-40">
                        <MaterialSymbol name="support" size={40} />
                        Community Analytic Assistant
                    </div>
                </div>
            </div>
        </div>
        <!-- Four -->
        <div class="quality flex flex-shrink-0 items-center w-full px-8">
            <div class="card flex flex-col gap-12 w-full py-8">
                <div class="header flex flex-col gap-8">
                    <Header>Unlock the Gateway to Seamless Connection</Header>
                    <span class="description text-xl font-medium max-lg:px-8">Tendopia opens the door to a seamless bridge between Web2 and Web3, where social interaction takes center stage. Dive into a world of boundless possibilities where connections flourish, communities thrive, and innovation knows no bounds. Join us and experience the power of social synergy like never before.</span>
                </div>
                <div class="cards flex flex-col w-full overflow-hidden gap-4">
                    {#each new Array(3).fill(null) as _, rowIndex (rowIndex)}
                        {@const items = rowIndex % 2 ? gateway : gateway2}
                        <div class="marquee flex gap-4 w-full odd:translate-x-20">
                            {#each items as item, index (index)}
                                <div class="card p-4 flex justify-center items-center gap-4">
                                    <div class="icon flex justify-center items-center w-10 h-10 rounded">
                                        <MaterialSymbol name="api" size={40} />
                                    </div>
                                    {item}
                                </div>
                            {/each}
                        </div>
                    {/each}
                </div>
            </div>
        </div>
        <!-- Five -->
        <!-- <div class="development flex flex-col flex-shrink-0 w-full px-8 gap-12">
            <div class="widgets grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8 w-full py-8">
                {#each devs as title, index (index)}
                    {@const [header, desc] = title.split(':')}
                    <div class="widget hover:brightness-150 transition-all card bg-transparent border-2 border-[#927EBC] p-4 flex flex-col justify-center items-center gap-2">
                        <span class="title text-2xl font-semibold">{header}</span>
                        <span class="desc">{desc}</span>
                    </div>
                {/each}
            </div>
        </div> -->
        <!-- Six -->
        <div class="roadmap flex flex-col flex-shrink-0 items-center w-full px-8 gap-12 lg:gap-20 ">
            <Header>Roadmap</Header>
            <div class="max-lg:card flex max-lg:flex-col max-lg:items-center gap-16 lg:gap-0 w-full max-lg:p-8 text-xl">
                {#each steps as step, index (step)}
                    {#if index !== 0}
                        {#if index % 2}
                            <Deco layout="lg:w-10 lg:my-auto lg:rotate-45 flex-shrink-0" />
                        {:else}
                            <Deco layout="lg:w-10 lg:my-auto lg:-rotate-45 flex-shrink-0" />
                        {/if}
                    {/if}
                    <div class="lg:card flex flex-col gap-16 lg:gap-2 lg:w-full lg:h-52 justify-center items-center p-8 lg:py-4" class:lg:mt-72={index % 2}>
                        <div class="header text-5xl font-medium lg:text-xl lg:font-semibold">
                            {step[0]}
                        </div>
                        <span class="description lg:text-sm">
                            {step[1]}
                        </span>
                    </div>
                {/each}
            </div>
        </div>
        <!-- Seven -->
        <div class="testimony flex flex-col flex-shrink-0 min-h-full w-full px-8 gap-12 justify-center">
            <Header>Our Team</Header>
            <div class="testimonies grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8 w-full py-8 text-left">
                {#each new Array(8).fill(null) as _, index (index)}
                    <div class="card p-4 flex flex-col gap-4 h-40">
                        <div class="user flex items-center gap-4">
                            <MaterialSymbol name="account_circle" size={40} />
                            <span>Nunya Bizz</span>
                        </div>
                        <div class="review">
                            wow this is so amazing
                        </div>
                    </div>
                {/each}
            </div>
        </div>
        <!-- Eight -->
        <div class="ai-powered flex flex-col flex-shrink-0 w-full gap-12 px-8">
            <Header>Partners & Backers</Header>
            <div class="cards w-fit mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-4 gap-4">
                {#each widgets as [icon], index (index)}
                    <div class="card hover:brightness-150 transition-all bg-transparent p-6 flex flex-col w-full min-w-32 min-h-32 xl:w-40 xl:h-40 justify-center items-center gap-6">
                        <MaterialSymbol name={icon} size={40} layout="flex flex-shrink-0 w-16 h-16 place-content-center text-[#927EBC] bg-purple-200/20 rounded-full" />
                        <span class="title font-semibold">AaAaAa</span>
                    </div>
                {/each}
            </div>
        </div>
        <Footer />
    </div>
</div>

<style lang="scss">
    .card:not(.widget),
    .icon {
        background: radial-gradient(rgb(255, 255, 255, .2), rgb(255, 255, 255, .05))
    }
</style>