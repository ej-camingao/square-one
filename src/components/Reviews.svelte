<script>
  import Conversion from "./Conversion.svelte";
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";
    

    let lim = true;

    let reviewsList = [
        {
            name: "Character",
            review: "We are a premier Cebu-based construction firm specializing in General Engineering and General Building. Established on May 8, 2015, we have swiftly earned a reputation for <span class='text-green-700 emphasis'>excellence, reliability, and innovation</span>.",
            icon: "fa-person-digging"
        },
        {
            name: "Commitment",
            review: "Our commitment to delivering <span class='text-green-700 emphasis'>quality workmanship with the highest safety standards</span> is evident in every project we undertake, from road and highway pavements to bridges, airports, irrigation systems, and recreational spaces.",
            icon: "fa-city"
        },
        {
            name: "Connections",
            review: "Licensed by the <span class='text-green-700 emphasis'>Philippine Contractors Accreditation Board (PCAB)</span> and a proud member of the <span class='text-green-700 emphasis'>Cebu Contractors Association, Inc.</span>, we serve both government and private sector clients with a diverse portfolio of successful projects.",
            icon: "fa-circle-nodes"
        },
        {
            name: "Capability",
            review: "Our team comprises <span class='text-green-700 emphasis'>licensed and experienced professionals</span> who have undergone rigorous training in construction safety and management, ensuring that we not only meet but exceed industry standards.",
            icon: "fa-hand-fist"
        },
    ];
</script>

<SectionWrapper id="about">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Blueprints Into <span class="text-green-700">Reality</span>
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                 About Us
            </h3>
        </div>

        <!-- <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div> -->

        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={false} {index} />
                {/each}
            </div>
        </div>

        <!-- <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button> -->
        <div class="w-full"><Conversion/></div>
        

    </div>
</SectionWrapper>