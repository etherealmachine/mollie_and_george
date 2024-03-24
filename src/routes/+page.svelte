<script lang="ts">
  const imgs: string[] = [];
  for (let i = 1; i <= 25; i++) {
    imgs.push(`images/mollie${i}.jpg`);
  }
  let currentImageIndex = 0;
  function updatePreviews(index: number): string[] {
    return imgs.slice(1, 6);
  }
  let previews: string[] = updatePreviews(currentImageIndex);
  $: previews = updatePreviews(currentImageIndex);
  $: console.log(previews);
</script>

<div class="w-full h-full flex flex-wrap justify-center gap-12">
  <div class="h-full flex flex-col mt-[5%]">
    <h1 class="text-6xl font-bold">Mollie Dent</h1>
    <aside>October 29, 1952 - Feb 6, 2024</aside>
    <figure class="mt-12">
      <img class="max-w-[524px]" src={imgs[currentImageIndex]} alt="Mollie Dent" />
      <figcaption>Dec 11, 2011</figcaption>
    </figure>
    <div class="flex gap-[6px] mt-2 items-center">
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
      {#each previews as img}
        <img class="max-w-[100px] hover:shadow-2xl hover:scale-110" src={img} alt="Mollie Dent - Preview" />
      {/each}
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
    </div>
  </div>
  <div class="flex flex-col max-w-[48ch] py-12">
    <h1 class="text-2xl font-bold">Recordum Vitae</h1>
    <aside>October 29, 1952 - Feb 6, 2024</aside>
    <section class="font-light leading-relaxed">
      <p>
Mollie Dent passed peacefully at her home in San Jose at the age of 71 after a
6-year battle with cancer. Born in Downey, California, she was the beloved first
daughter of Betty and Thomas Dent. Mollie is now reunited with her loving
parents and her husband, George Pettit. She is survived by her younger sister,
Sherri, her stepson, Michael, and her son, James Pettit.
      </p>
      <p>
The family moved to Santa Clara, where Mollie attended primary school. She
demonstrated intelligence and wit from an early age. Mollie graduated in 1974
from San Jose State University before pursuing a law degree from UC Law, San
Francisco. After practicing law in Livermore and San Jose, Mollie moved to
Juneau, Alaska to combine her work with her love of the outdoors. In Alaska,
she worked for the Sierra Club Legal Defense Fund, helping to protect many wild
spaces like Admiralty Island and the Arctic National Wildlife Refuge. While in
Juneau she also married George Pettit in May of 1981, whom she met on a Sierra
Club hike. Mollie and George moved to Dallas, TX in 1983 where she gave birth to
her son. In 1987, they moved back to settle in San Jose where she began her long
career working for the San Jose City Attorney’s Office.
      </p>
      <p>
Mollie was a devoted mother and a diligent attorney. She enjoyed going to the
theater, camping all across the United States, and traveling to Great Britain
and Europe. In the Bay Area she loved hiking, skiing, gardening, and was an avid
reader. She developed strong life-long bonds with her many friends, coworkers,
and caregivers who have all given tremendous support to her in the last few
years.
      </p>
      <p>
A memorial service and celebration of life will be held at Vasona Lake County
Park in Los Gatos on May 5th, please contact James Pettit to RSVP. If you wish
to make a gift to commemorate her life, please consider Doctors Without Borders,
Earth Justice, Playful People Productions and Hearts & Minds Activity Center.
      </p>
    </section>
  </div>
</div>