<script>
  import { isOverlayOpen } from "../store";


</script>

<div class="w-screen h-screen fixed top-0 left-0 flex justify-center bg-black-100 opacity-90 z-30">
  <div class="w-screen bg-gray-900 text-white rounded-md px-8 gray-10 relative max-w-lg">
  <button class="absolute top-2 right-3 text-3xl text-gray-300 hover:-translate-y-0.5 transition-transform" on:click={() => isOverlayOpen.set(false)}>&times;</button>
    <slot/>
  </div>

</div>