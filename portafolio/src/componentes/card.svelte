<script>
    export let nameProyect;
    export let img;
    export let description;

    let showDesc = false;

    function showDescription(){
        showDesc = !showDesc;
    }
</script>

<button id="buttonCard" on:mouseenter={showDescription} on:mouseleave={showDescription}>
    <img src={img} alt="">
    {#if showDesc}
        <div id="contentCard" data-aos="fade-left">
            <h3>{nameProyect}</h3>
            <p>{description}</p>
        </div>
    {/if}
</button>

<style>
    #buttonCard{
        width: 100px;
        height: 100px;
        background-color: transparent;
        border: none;
        display: flex;
        flex-direction: row;
    }
    #contentCard{
        width: 50%;
        height: 100%;
        background: linear-gradient(right, transparent, #000);
    }
</style>