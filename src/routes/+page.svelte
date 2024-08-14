<script>
    import Conversion from "../components/Conversion.svelte";
import FAQs from "../components/FAQs.svelte";
    import Hero from "../components/Hero.svelte";
    import Product from "../components/Product.svelte";
    import Reviews from "../components/Reviews.svelte";

</script>
<!-- <h1 class="text-green-400">Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->

<main class="flex flex-col">
    <Hero />
    <Product />
    <Reviews />
    <FAQs/>
    <Conversion/>
</main>