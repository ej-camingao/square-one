<script>
    import Carousel from "./Carousel.svelte";
import CtAs from "./CTAs.svelte";
    import Header from "./Header.svelte";
    import SectionHero from "./SectionHero.svelte";

</script>
<SectionHero>
    <Header/>
    <div
    class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
>
    <h2 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold logo_text">
        SQUARE ONE <span class="text-green-700">BUILDERS</span>
        <br/>
        <!-- Just Got a <span class="text-green-700">Wesbite</span> -->
    </h2>
    <!-- <p class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full">
    less worry, <span class="italic">more building</span>
    </p> -->
    <!-- <CtAs/> -->
    <!-- <div class="flex items-center justify-center gap-2 text-base">
        {#each [0] as index }
            <div class="grid place-items-center relative">
                <i class="fa-solid fa-star opacity-0"></i>
                <div class={"absolute top-0 left-0 grid place-items-center" + (index==4 ? "width [60%] overflow-hidden" : " ")}>
                    <i class="fa-solid fa-hammer text-amber-400"></i>
                </div>
            </div>
        {/each}
    </div> -->
        
    

    </div>

    <div class="gap-2 text-base mb-20"><Carousel/></div>


</SectionHero>