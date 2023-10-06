<script context="module">
    let count = 3;
    
    export let isFilled = [];
    for(let i = 0; i < count; i ++) {
        isFilled[i] = false
    }

</script>

<div class="dice">
    <span on:click={() => d10Click(0)}><i class="{isFilled[0] ? "d10Fill" : "d10"}"></span>
    <span on:click={() => d10Click(1)}><i class="{isFilled[1] ? "d10Fill" : "d10"}"></span>
    <span on:click={() => d10Click(2)}><i class="{isFilled[2] ? "d10Fill" : "d10"}"></span>
</div>

<script>
    function d10Click(i) {
        isFilled[i] = !isFilled[i];
        console.log(isFilled[i]);
    }
</script>

<style>
    .dice {
        height: 4em;
        width: auto;
        color: pink;
        border-radius: 15%;
    }

    .d10 {
        content: url("../icons/dice-d10.svg");
        display: inline;
        height: 1em;
        width: auto;
    }

    .d10:hover {
        content: url("../icons/dice-d10-filled.svg");
        display: inline;
        height: 1em;
        width: auto;
        opacity: 0.5;
    }

    .d10Fill {
        content: url("../icons/dice-d10-filled.svg");
        display: inline;
        height: 1em;
        width: auto;
        color: black;
    }
</style>

