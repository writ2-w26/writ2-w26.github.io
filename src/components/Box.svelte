<script>
    let { checked = $bindable() } = $props();
</script>

<div class="contents">
    <p class="title">Settings</p>
    <div class="list">
        <div class="toggle">
            Show Contributors
            <input type="checkbox" bind:checked={checked}/>
        </div>
        <div class="people" class:hidden={!checked}>
            <span class="attr all">All</span>
            <span class="attr h">Huang, J.</span>
            <span class="attr m">Man, A.</span>
            <span class="attr l">Lin, J.</span>
        </div>
    </div>
</div>

<style>
    .hidden {
        opacity: 0;
        max-height: 0;
    }
    .people {
        transition: opacity 0.2s cubic-bezier(0.16, 1, 0.3, 1), height 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        display: flex;
        max-width: 120px;
        flex-wrap: wrap;
        box-sizing: border-box;
        span {
            padding: 4px 6px;
            border-radius: 100px;
            margin-top: 4px;
            margin-right: 4px;
            &.all {
                border: 1px solid rgb(0 0 0 / 50%);
                background: rgb(0 0 0 / 20%);
            }
            &.h {
                border: 1px solid rgb(0 150 150 / 50%);
                background: rgb(0 150 150 / 20%);
            }
            &.m {
                border: 1px solid rgb(150 0 150 / 50%);
                background: rgb(150 0 150 / 20%);

            }
            &.l {
                border: 1px solid rgb(150 150 0 / 50%);
                background: rgb(150 150 0 / 20%);
            }
        }
    }
    .toggle {
        display: flex;
        gap: 8px;
    }
    .contents {
        font-family: InterVariable, sans-serif;
        background: white;
        float: right;
        margin: 0 0 0 16px;
        border: 1px solid rgb(0 0 0 / 20%);
        border-radius: 10px;
        line-height: 1;
        font-size: 0.8rem;
        overflow: hidden;
        .list {
            display: flex;
            flex-direction: column;
            padding: 8px 10px;
        }
        .title {
            background: #FDC700;
            padding: 8px 10px;

            font-weight: bold;
        }
    }
    * {
        font-family: InterVariable, sans-serif;
    }
</style>