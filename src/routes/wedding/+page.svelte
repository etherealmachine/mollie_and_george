<script lang="ts">
  import Carousel from "$lib/Carousel.svelte";

  const images: any[] = [];
  for (let i = 1; i <= 40; i++) {
    images.push({
      index: i-1,
      src: `/images/wedding/wedding${i}.webp`,
      caption: '',
    });
  }
</script>

<div class="flex flex-wrap justify-center gap-6 md:gap-12 px-4 mb-6">
  <div class="flex flex-col items-center mt-[5%]">
    <Carousel images={images} />
  </div>
</div>