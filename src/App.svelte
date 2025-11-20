<script lang="ts">
    import Logo from "./assets/noblar/noblar-cut.png";
    import ContactWhatsapp from "./lib/contact-whatsapp.svelte";
    import ProductList from "./lib/product-list.svelte";
</script>

<header class="flex justify-between mx-4 lg:mx-12 mt-4 lg:mt-8">
    <!-- <img class="w-8 h-8" src="assets/images/noblar-logo.png" alt=""> -->
    <div></div>

    <nav class="flex items-center text-noblar text-2xl">
        <i class="fa-brands fa-facebook mr-4"></i>
        <i class="fa-brands fa-instagram mr-4"></i>
        <a href="https://www.tiktok.com/@noblar.wood" title="Noblar TikTok">
            <i class="fa-brands fa-tiktok"></i>
        </a>
    </nav>
</header>

<div class="flex flex-col items-center text-center mt-6 md:mt-4">
    <!-- <h1 class="metallic text-6xl lg:text-9xl font-extrabold tracking-widest">Noblar</h1> -->
    <div class="w-xs md:w-md">
        <img src={Logo} alt="Noblar" />
    </div>

    <div class="fancy-line mt-6 w-xs md:w-2xl"></div>

    <p class="mt-4 text-sm text-noblar">
        Artă în lemn masiv. Elemente decorative din stejar nobil, create cu pasiune și precizie. <br/>
        Fiecare piesă spune o poveste.
    </p>

    <div class="mt-2">
        <ContactWhatsapp text="Buna ziua, sunt interesat de un produs din oferta dumneavoastra" />
    </div>
</div>

<ProductList />
