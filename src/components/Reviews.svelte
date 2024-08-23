<script>
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";

    let lim = true;

    let reviewsList = [
        {
            name: "John Doe",
            review: "Square One Builders exceeded our expectations on our home renovation project. Their attention to detail and commitment to quality were evident from start to finish. Highly recommend!",
            features: [
                "Excellent Service"
            ],
        },
        {
            name: "Jane Smith",
            review: "We couldn't be happier with the commercial space Square One Builders completed for us. They delivered on time and on budget, and the finished product is fantastic. Their professionalism is unmatched.",
            features: [
                "Budget Friendly",
            ],
        },
        {
            name: "Michael Brown",
            review: "The team at Square One Builders did an outstanding job on our new bridge construction. Their expertise and efficient project management ensured everything was completed safely and on schedule.",
            features: [
                "Accomodating"
            ],
        },
        {
            name: "Sarah Williams",
            review: "Square One Builders transformed our outdated office building into a modern, functional space. Their innovative design solutions and top-notch craftsmanship made all the difference.",
            features: [
                "Attention to Detail"
            ],
        },
        {
            name: "Ashley Johnson",
            review: "We entrusted Square One Builders with our school renovation, and they delivered exceptional results. The project was completed with minimal disruption, and the new facilities are a tremendous improvement.",
            features: [
                "Timely Outputs",
            ],
        },
        {
            name: "Mark Robinson",
            review: "Square One Builders handled our highway expansion project with remarkable efficiency and skill. Their dedication to quality and safety was evident throughout, making the entire process smooth and successful.",
            features: [
                "Efficient"
            ],
        },
    ];
</script>

<SectionWrapper id="reviews">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Don't just take our word for it
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                See What <span class="text-green-700">Others</span> Have To Say
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
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
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button>
        <div class="flex flex-col gap-10">
            <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
                Trusted by
            </p>
            <div class="flex flex-wrap justify-center gap-8">
                <!-- Example logos -->
                <img src="assets/comLogo1.png" alt="Company 1 Logo" class="h-12 md:h-16 object-contain">
                <img src="assets/comLogo2.png" alt="Company 2 Logo" class="h-12 md:h-16 object-contain">
                <img src="assets/comLogo3.png" alt="Company 3 Logo" class="h-12 md:h-16 object-contain">
                <!-- Add more logos as needed -->
            </div>
            <!-- <Stars /> -->
        </div>
    </div>
</SectionWrapper>