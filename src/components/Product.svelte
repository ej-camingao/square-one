<script>
    import ProductCard from "./ProductCard.svelte";
import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                "Square One Builders is a contractor company with a strong focus on infrastructure projects, including the construction of highways and bridges. Their expertise in large-scale projects ensures durable, high-quality structures that enhance connectivity and support community development."
            ],
            description: '',
            imgUrl: 'assets/prod1.png'
        },
        {
            featureList: [
                "Square One Builders is a trusted contractor company with extensive experience in institutional projects, including schools, hospitals, and government buildings. Their focus on quality construction and timely delivery ensures that these vital facilities are built to serve communities effectively and sustainably."
            ],
            description: '',
            imgUrl: 'assets/prod2.png'
        },
        {
            featureList: [
                "Square One Builders is a premier contractor company specializing in high-quality residential projects, known for their meticulous attention to detail and innovative designs. They are dedicated to transforming homes with exceptional craftsmanship and personalized service, ensuring every project exceeds client expectations."
            ],
            description: '',
            imgUrl: 'assets/prod3.png'
        }
    
    ]

</script>
<SectionWrapper id="product">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">Building Your 
                <span class="text-green-700"> Foundation</span>
            </p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">Projects</h3>
                {#each productFeatures as productFeature, index}
                    <ProductCard productFeature={productFeature} index={index}>
                        {#if index===0}
                        <span class="text-green-700 font-medium">Infrastructure</span> Projects
                        {:else if index===1}
                        <span class="text-green-700 font-medium">Institutional</span> Construction
                        {:else}
                        <span class="text-green-700 font-medium">Residential</span> Units
                        {/if}
                    </ProductCard>
                {/each}
        </div>
    </div>
</SectionWrapper>