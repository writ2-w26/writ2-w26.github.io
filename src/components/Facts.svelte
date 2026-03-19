<script>
    let { content, image } = $props();
</script>

<div class="container">
    <div class="text">
        <h4>Fun Facts</h4>
        <span>{@html content}</span>
    </div>
    <img src={image} alt=""/>
</div>

<style>
    img {
        display: block;
        width: 200px;
        object-fit: cover;
    }
    .container {
        margin-bottom: 10px;
        border: 1px solid rgb(0 0 0 / 20%);
        border-radius: 10px;
        display: flex;
        justify-content: space-between;
        overflow: hidden;
        flex-wrap: wrap;
    }
    .text {
        padding: 14px 14px 10px 14px;
        line-height: 1;
        font-family: InterVariable, sans-serif;
        text-align: left;
        max-width: 370px;
        min-width: 200px;
        flex: 1;
        h4 {
            margin-bottom: 4px;
        }
        span {
            font-size: 0.8em;
            line-height: 1.5;
            :global(>*) {
                padding-inline-start: 16px;
            }
        }
    }
</style>