<script>
    export let nameProyect;
    export let img;
    export let description;
    export let link;
    export let width;
    export let height;
  
    let showDesc = false;
  
    function showDescription() {
      showDesc = !showDesc;
    }
  </script>
  
  <button id="buttonCard" style="background-image: url({img}); background-size: cover; width: {width}px; height:{height}px;">
    <a href={link} id="linkCard" on:mouseenter={showDescription} on:mouseleave={showDescription}>
      {#if showDesc}
        <div id="contentCard" data-aos="fade-left">
            <div id="textoCard">
                <h3>{nameProyect}</h3>
                <p>{description}</p>
            </div>
        </div>
      {/if}
    </a>
  </button>
  
  <style>
    #buttonCard {
      background-color: transparent;
      border: none;
      display: flex;
      flex-direction: row;
    }
    #contentCard {
      width: 100%;
      height: 100%;
      background: linear-gradient(to left, transparent, #000);
    }
    #contenidoIMG {
      width: 100%;
    }
    #linkCard {
      text-decoration: none;
      height: 100%;
      width: 100%;
    }
    #contentCard.showDesc {
      background-color: black;
    }
    #textoCard{
        width: 50%;
        height: 100%;
        color: white;
    }
  </style>
  