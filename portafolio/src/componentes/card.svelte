<script>
    import { onMount } from 'svelte';

    export let nameProyect;
    export let img;
    export let description;
    export let link;
    export let width;
    export let height;

    onMount(() => {
        if(width == undefined && height == undefined){
            width = 100;
            height = 100;
        }
        const buttonCard = document.getElementById('buttonCard');
        buttonCard.style.width = width + 'px';
        buttonCard.style.height = height + 'px';
    });

    

    let showDesc = false;

    function showDescription(){
        showDesc = !showDesc;
    }
</script>

<button id="buttonCard" on:mouseenter={showDescription} on:mouseleave={showDescription}>
    <a href={link}>
        <img src={img} alt="">
        {#if showDesc}
            <div id="contentCard" data-aos="fade-left">
                <h3>{nameProyect}</h3>
                <p>{description}</p>
            </div>
        {/if}
    </a>
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