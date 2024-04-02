<script lang="ts">
  interface Image {
    index: number
    src: string
    thumb: string
    caption: string
  }
  export let images: Image[];
  let i = 0;
  const thumbnails: HTMLImageElement[] = [];
  function updateFocus(i: number) {
    if (thumbnails[i]) {
      thumbnails[i].scrollIntoView({ behavior: "smooth", block: "nearest", inline: "center" });
    }
  }
  $: updateFocus(i);
</script>

<figure>
  <img
      class="md:max-w-[595px] max-h-[438px] object-contain"
      src={images[i].src}
      alt={images[i].caption} />
  <figcaption>{images[i].caption}</figcaption>
</figure>
<div class="flex gap-[6px] mt-2">
  <button on:click={() => { i--; if (i < 0) { i = images.length-1 } } }>
    <svg
        width="24px"
        height="24px"
        stroke-width="1.5"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        color="#000000">
      <path
          d="M15 6L9 12L15 18"
          stroke="#000000"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round" />
    </svg>
  </button>
  <div
      class="md:max-w-[525px] flex gap-[6px] overflow-scroll p-2">
    {#each images as img, index }
      <img
          bind:this={thumbnails[index]}
          class="w-[100px] h-[75px] object-contain outline-emerald-600 outline-2 hover:outline hover:outline-emerald-500 hover:outline-2"
          class:outline={i === index}
          on:click={() => { i = index } }
          src={img.thumb}
          alt={img.caption} />
    {/each}
  </div>
  <button on:click={() => { i++; if (i >= images.length) { i = 0 } } }>
    <svg
        width="24px"
        height="24px"
        stroke-width="1.5"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        color="#000000">
      <path
          d="M9 6L15 12L9 18"
          stroke="#000000"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round" />
    </svg>
  </button>
</div>