<script>
    import Carousel from 'svelte-carousel';
    import { browser } from '$app/environment';

  let carousel; // for calling methods of the carousel instance
  
  const handleNextClick = () => {
    carousel.goToNext()
  }
</script>

{#if browser}
  <Carousel
    bind:this={carousel}
	autoplay
	autoplayDuration={7000}
	autoplayProgressVisible={false}
	pauseOnFocus
	arrows={false}
	dots={false}
  >
    <div class="justify-items-center">
		<h4 class="text-xl sm:text-s md:text-m lg:text-2xl max-w-[1200px] mx-auto w-full text-center font-semibold italic text-green-900">MISSION</h4>
		<p class="text-l sm:text-s md:text-m text-center max-w-[1000px] mx-auto w-full italic">
		To deliver superior construction services with a steadfast commitment to quality workmanship, safety standards, and environmental responsibility, ensuring the success and satisfaction of our clients through innovative and cost-effective solutions.
		</p></div>
    <div class="justify-items-center">
		<h4 class="text-xl sm:text-l md:text-2l lg:text-2xl max-w-[1200px] mx-auto w-full text-center font-semibold italic text-green-900">VISION</h4>
		<p class="text-l sm:text-s md:text-m text-center max-w-[1000px] mx-auto w-full italic">
		To be a leading construction firm recognized for excellence, integrity, and reliability, shaping the landscape of Cebu and beyond with our innovative engineering solutions and unwavering commitment to safety and sustainability.
		</p></div>
  </Carousel>
{/if}

<!-- <button on:click={handleNextClick}>Next</button> -->