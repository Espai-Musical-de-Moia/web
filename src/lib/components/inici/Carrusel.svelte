<script>
  import { onMount, onDestroy } from "svelte";
  import image_1 from "$lib/img/carrusel/orquestra_1.png";
  import image_2 from "$lib/img/carrusel/orquestra_2.png";
  import image_3 from "$lib/img/carrusel/orquestra_3.png";
  import image_4 from "$lib/img/carrusel/orquestra_4.png";

  let images = [image_1, image_2, image_3, image_4];

  let currentIndex = 0;

  function nextImage() {
    currentIndex = (currentIndex + 1) % images.length;
  }

  let interval2;

  onMount(() => {
    interval2 = setInterval(nextImage, 3000);
  });
</script>

<div class="carrusel">
  {#each images as image, index}
    <img
      src={image}
      alt="Carrusel Images"
      style="display: {index === currentIndex ? 'block' : 'none'}"
    />
  {/each}
</div>

<style>
  .carrusel {
    width: 60%;
    margin: 0 auto;
    overflow: hidden;
    padding-bottom: 5.5%;
  }

  .carrusel img {
    width: 100%;
    height: 28vw;
    object-fit: cover;
    border-radius: 2%;
    margin-top: 14%;
  }

  @media screen and (max-width: 575x) {
    .carrusel {
      width: 60%;
      margin: 0 auto;
      overflow: hidden;
      padding-bottom: 2.5%;
    }

    .carrusel img {
      width: 100%;
      height: 20vw;
      object-fit: cover;
      border-radius: 2%;
      margin-top: -10%;
    }
  }
  @media screen and (min-width: 768px) and (max-width: 991px) {
    .carrusel img {
      width: 100%;
      height: 20vw;
      object-fit: cover;
      border-radius: 2%;
      margin-top: -10%;
    }
   }
</style>
