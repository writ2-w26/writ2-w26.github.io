<script>
    let closed = $state(true);
</script>

<svelte:window onkeydown={(e) => e.key === 'Escape' ? closed = true : null}/>
<button onclick={() => {closed = !closed}}>View Sources</button>
<!-- svelte-ignore a11y_no_static_element_interactions, a11y_click_events_have_key_events -->
<div class="container" class:disabled={closed} onclick={() => { closed = true } }>
    <div class="dialog" onclick={(e) => { e.stopPropagation() }} >
        <div class="bar">
            <h2>Sources</h2>
            <button onclick={() => {closed = true}}>✕</button>
        </div>
        <div class="citations">
            <p>Zewe, Adam. “Explained: Generative AI’s Environmental Impact.” MIT News, Massachusetts Institute of Technology, 17 Jan. 2025, https://news.mit.edu/2025/explained-generative-ai-environmental-impact-0117.</p>
            <p>United Nations Environment Programme. “AI Has an Environmental Problem. Here’s What the World Can Do about That.” UNEP, https://www.unep.org/news-and-stories/story/ai-has-environmental-problem-heres-what-world-can-do-about.</p>
            <p>Dauner, Maximilian, and Gudrun Socher. “Energy Costs of Communicating with AI.” Frontiers in Communication, vol. 10 2025, https://www.frontiersin.org/journals/communication/articles/10.3389/fcomm.2025.1572947/full.</p>
            <p>Storrow, Benjamin. “To Feed Data Centers, Pennsylvania Faces a New Fracking Surge.” Yale Environment 360, Yale School of the Environment, https://e360.yale.edu/features/pennsylvania-data-centers-natural-gas.</p>
            <p>Nutt, David. “‘Roadmap’ Shows the Environmental Impact of AI Data Center Boom.” Cornell Chronicle, 10 Nov. 2025, https://news.cornell.edu/stories/2025/11/roadmap-shows-environmental-impact-ai-data-center-boom.</p>
            <p>IEA. “Digitalisation and Energy.” International Energy Agency, 2017, www.iea.org/reports/digitalisation-and-energy.</p>
            <p>Crawford, Kate. The Atlas of AI: Power, Politics, and the Planetary Costs of Artificial Intelligence. Yale University Press, 2021. JSTOR, https://www.jstor.org/stable/j.ctv1ghv45t.</p>
            <p>Jones, Nicola. “How to Stop Data Centres from Gobbling Up the World’s Electricity.” Nature, vol. 561, no. 7722, 2018, pp. 163–166, https://www.nature.com/articles/d41586-018-06610-y.</p>
            <p>Hao, Karen. “Training a Single AI Model Can Emit as Much Carbon as Five Cars in Their Lifetimes.” MIT Technology Review, 6 June 2019, https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/.</p>
            <p>Wang, Qiang, Yuanfan Li, and Rongrong Li. “Ecological Footprints, Carbon Emissions, and Energy Transitions: The Impact of Artificial Intelligence (AI).” Humanities and Social Sciences Communications, vol. 11, 2024, Article 1043, https://www.nature.com/articles/s41599-024-03520-5.</p>
            <p>Girolimon, Mars. “Understanding the Environmental Impact of AI | SNHU.” Southern New Hampshire University, 6 January 2026, https://www.snhu.edu/about-us/newsroom/stem/ai-environmental-impact.</p>
            <p>O’Donnell, James. “AI’s Emissions Are About To Skyrocket Even Further.” MIT Technology Review, 16 Dec. 2024, https://www.technologyreview.com/2024/12/13/1108719/ais-emissions-are-about-to-skyrocket-even-further.</p>
            <p>Nicoletti, Leonardo, et al. “How AI Demand Is Draining Local Water Supplies.” Bloomberg, 8 May 2025, www.bloomberg.com/graphics/2025-ai-impacts-data-centers-water-data/</p>
            <p>De Mott, Filip. “AI Will Nearly Double Demand for Copper, Which Is Already Facing a Global Shortage.” Markets Insider, 16 Sept. 2024, https://markets.businessinsider.com/news/commodities/copper-shortage-commodity-price-artificial-intelligence-outlook-data-centers-ai-2024-9.</p>
            <p>Wilkins, Joe. “First Responders Are Being Overwhelmed by Data Center Fires.” Futurism, 28 Sept. 2025, futurism.com/future-society/fire-fighters-data-centers.</p>
        </div>
    </div>
</div>

<style>
    .disabled {
        opacity: 0;
        pointer-events: none;
    }
    .citations {
        padding-inline: 4px;
        overflow: scroll;
        flex: 1;
        p {
            margin-bottom: 8px;
        }
    }
    .dialog {

        background: white;
        width: calc(100vw - 64px);
        padding: 16px;
        border-radius: 32px;
        max-width: 600px;
        box-sizing: border-box;
        height: calc(100vh - 64px);
        display: flex;
        flex-direction: column;
        overflow-wrap: break-word;
        position: relative;
        button {
            flex: 0;
            width: 2rem;
            height: 2rem;
            padding: 8px;
            aspect-ratio: 1;
            display: grid;
            place-items: center;
            line-height: 1;
        }
        .bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 8px;
        }
        h2 {
            font-family: InterVariable, sans-serif;
            flex: 1;
            padding-inline: 4px;
        }
    }
    .container {
        transition: opacity 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        position: fixed;
        top: 0;
        left: 0;
        background: rgb(0 0 0 / 20%);
        width: 100%;
        height: 100%;
        backdrop-filter: blur(20px);
        display: grid;
        place-items: center;
    }
    button {
        font-family: InterVariable, sans-serif;
        border: none;
        background: rgb(0 0 0 / 20%);
        width: 100%;
        padding: 16px;
        cursor: pointer;
        border-radius: 16px;
        margin-bottom: 16px;
    }
</style>