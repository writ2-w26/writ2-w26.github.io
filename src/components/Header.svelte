<script>
    const icons = {
        calendar: "M200-80q-33 0-56.5-23.5T120-160v-560q0-33 23.5-56.5T200-800h40v-80h80v80h320v-80h80v80h40q33 0 56.5 23.5T840-720v560q0 33-23.5 56.5T760-80H200Zm0-80h560v-400H200v400Z",
        author: "M560-120v-123l221-220q9-9 20-13t22-4q12 0 23 4.5t20 13.5l37 37q8 9 12.5 20t4.5 22q0 11-4 22.5T903-340L683-120H560Zm-400-40v-112q0-34 17.5-62.5T224-378q62-31 126-46.5T480-440q37 0 73 4.5t72 14.5L480-276v116H160Zm663-184 37-39-37-37-38 38 38 38ZM367-527q-47-47-47-113t47-113q47-47 113-47t113 47q47 47 47 113t-47 113q-47 47-113 47t-113-47Z",

    }
</script>

<header>
    <div class="bg">
        <!--div class="text">
            <h1>Title here: something something</h1>
            <p class="attribution">
                <svg viewBox="0 -960 960 960" height="1rem"><path d={icons.calendar}/></svg>
                March 15, 2026
                &nbsp;
                <svg viewBox="0 -960 960 960" height="1rem"><path d={icons.author}/></svg>
                Jeffrey Huang, Jeffrey Lin, Alan Man
            </p>
        </div-->
    </div>
</header>

<style>
    svg {
        opacity: 50%;
    }
    .text {
        position: absolute;
        bottom: 32px;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
        align-items: center;
        flex-direction: column;
        width: 100%;
        filter: drop-shadow(0 4px 8px rgb(0 0 0 / 50%));
    }
    h1 {
        background: white;
        text-align: center;
        font-family: "InterVariable", sans-serif;
        padding: 4px 8px;
        border-radius: 8px;
        width: fit-content;
        box-sizing: border-box;
    }
    .attribution {
        margin-top: -4px;
        width: fit-content;
        padding: 6px 8px;
        border-radius: 0 0 8px 8px;
        background: white;
        text-align: center;
        color: rgb(0 0 0 / 50%);
        font-size: 0.8rem;
        font-family: "InterVariable", sans-serif;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2px;
        box-sizing: border-box;
    }
    header {
        max-width: 800px;
        margin: 0 auto;
        height: 300px;
        position: relative;
        padding: 16px;
        box-sizing: border-box;
        .bg {
            background-image: url('/t.jpeg');
            border-radius: 16px;
            width: 100%;
            height: 100%;
            background-position: center;
            background-size: cover;
        }
    }
</style>