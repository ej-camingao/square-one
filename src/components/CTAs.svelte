<script>
  import Carousel from "./Carousel.svelte";

    // export let dark;

    import {isOverlayOpen} from '../store'
</script>

<div class="flex items-center gap-4">
    <!-- <button class={"specialBtn " + (dark ? " bg-[#181b34]" : " ")}>
        <p class="text-base sm:text-lg md:text-xl">Contact Us</p>
    </button> -->
    <!-- {$isOverlayOpen} -->
    <button class="specialBtnDark" on:click={() => {isOverlayOpen.set(true)}}>
        <p class="text-base sm:text-lg md:text-xl">
            Contact Us
        </p>
    </button>
</div> 