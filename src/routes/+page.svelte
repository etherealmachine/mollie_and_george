<script lang="ts">
  const imgs: string[] = [];
  for (let i = 1; i <= 25; i++) {
    imgs.push(`images/mollie${i}.jpg`);
  }
</script>

<div>
  {#each imgs as img}
    <img class="w-[512px]" src={img} />
  {/each}
</div>