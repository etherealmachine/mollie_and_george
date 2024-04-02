<script lang="ts">
  import Carousel from "$lib/Carousel.svelte";

  const images: any[] = [];
  for (let i = 1; i <= 25; i++) {
    images.push({
      index: i-1,
      src: `/images/mollie/mollie${i}.webp`,
      caption: '',
    });
  }
</script>

<div class="flex flex-wrap justify-center gap-6 md:gap-12 px-4 mb-6">
  <div class="flex flex-col mt-[5%]">
    <h1 class="text-2xl md:text-6xl font-bold">Mollie Dent</h1>
    <aside class="mb-4 md:mb-12">October 29, 1952 - February 6, 2024</aside>
    <Carousel images={images} />
  </div>
  <div class="flex flex-col max-w-[48ch] md:py-12 gap-2">
    <h1 class="text-2xl font-bold">Recordum Vitae</h1>
    <section class="font-light leading-relaxed text-lg">
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
Park in Los Gatos on May 5th, please contact
<a class="underline text-blue-800" href="mailto:james.l.pettit@gmail.com">James Pettit</a>
to RSVP. If you wish to make a gift to commemorate her life, please consider
Doctors Without Borders, Earth Justice, Playful People Productions and Hearts &
Minds Activity Center.
      </p>
    </section>
  </div>
</div>