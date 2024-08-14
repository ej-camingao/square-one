<script>
    import ProductCard from "./ProductCard.svelte";
import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                "Daily Checks",
                "Weighted Regression",
            ],
            description: 'Square One Builders is grounded in Integrity',
            imgUrl: 'assets/selection.png'
        },
        {
            featureList: [
                "Daily Checks",
                "Weighted Regression",
            ],
            description: 'Square One Builders is grounded in Truth',
            imgUrl: 'assets/training.png'
        },
        {
            featureList: [
                "Daily Wows",
                "Beautiful Builds",
            ],
            description: 'Square One Builders is grounded in Love',
            imgUrl: 'assets/goal.png'
        }
    
    ]

</script>
<SectionWrapper id="product">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">Build Your 
                <span class="text-green-700"> Foundation</span>
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">Features For Everyone</h3>
                {#each productFeatures as productFeature, index}
                    <ProductCard productFeature={productFeature} index={index}>
                        {#if index===0}
                        Experience a beginner exercise <span class="text-indigo-400 font-medium">master</span> class
                        {:else if index===1}
                        Lay the foundation for <span class="text-indigo-400 font-medium"> routine</span> and consistency
                        {:else}
                        Workouts specific to your <span class="text-indigo-400 font-medium">environment</span> and <span class="text-indigo-400 font-medium">expertise</span>
                        {/if}
                    </ProductCard>
                {/each}
        </div>
    </div>
</SectionWrapper>