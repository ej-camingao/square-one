<script>
    import {openModal} from '../store'
</script>

<header class="flex flex-col relative z-20">
    <div class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6">
        <a href="/">
        <!-- <h1 class="font-semibold">Square One <span class="text-green-700">Builders </span></h1> -->
        <img src="assets/Square_One Logo.png" alt="Square One Builders logo" class="max-w-[40px]"/>
        </a>
        <button on:click={() => ($openModal = true)} class="md:hidden grid place-items-center">
            <i class="fa-solid fa-bars" style="color: #63E6BE;"></i>
        </button>
        <nav class="hidden md:flex items-center gap-4 lg:gap-6">
            <a href="#product"class="duration-200 hover:text-green-700 cursor-pointer">Projects</a>
            <a href="#reviews"class="duration-200 hover:text-green-700 cursor-pointer">Reviews</a>
            <!-- <a href="#faqs"class="duration-200 hover:text-green-700 cursor-pointer">FAQ</a> -->
            <button class="specialBtn">
                <p>Contact Us</p>                    
            </button>
        </nav>
    </div>
</header>