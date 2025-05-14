<script lang="ts">
    let Shoe = $state('thumbnail-shoe1.svg');
    // let Shoe = 'thumbnail-shoe1.svg';
    function changeShoe(shoe:any) {
        console.log(shoe)
        Shoe = shoe;
    }
</script>

<div class="mx-5">
    <header class="container mx-auto mt-5">
        <nav class="flex justify-between items-center">
            <img src="/nikeapp/images/header-logo.svg" alt="">
            <div class="hidden xl:flex gap-15 *:text-bookmark-grey text-xl">
                <h2>Home</h2>
                <h2>About Us</h2>
                <h2>Products</h2>
                <h2>Contact Us</h2>
            </div>
            <h2 class="hidden xl:block text-xl xl:pr-5">Sign in / Explore now</h2>
            <!-- svelte-ignore a11y_consider_explicit_label -->
            <button class="xl:hidden">
                <i class="text-2xl fa-solid fa-bars hover:cursor-pointer"></i>
            </button>
        </nav>
    </header>

    <section class="container mx-auto mt-20 xl:flex justify-between">
        <div class="xl:w-[50%]">
            <p class="text-nike-orange text-xl">Our Summer collections</p>
            <h1 class="mt-10 font-palanquin text-8xl font-[500] leading-[106px] xl:bg-white xl:mt-5">The New Arrival </h1><br> 
            <h1 class="font-palanquin text-8xl font-[500]"><span class="text-nike-orange">Nike</span> Shoes</h1>
            <p class="text-xl text-bookmark-grey mt-8">Discover stylish Nike arrivals, quality <br>comfort, and innovation for your active life.</p>
            <button class="bg-nike-orange text-white mt-10 px-5 py-3 rounded-l-full rounded-r-full flex items-center">Shop Now <i class="ml-3 fa-solid fa-arrow-right"></i></button>
            <div class="flex justify-between mt-10 max-w-[25rem]">
                <div>
                    <h1 class="mt-10 font-palanquin text-5xl font-[500]">1k+</h1>
                    <p class="text-l text-bookmark-grey mt-2">Brands</p>
                </div>
                <div>
                    <h1 class="mt-10 font-palanquin text-5xl font-[500]">500+</h1>
                    <p class="text-l text-bookmark-grey mt-2">Shops</p>
                </div>
                <div>
                    <h1 class="mt-10 font-palanquin text-5xl font-[500]">250k+</h1>
                    <p class="text-l text-bookmark-grey mt-2">Customers</p>
                </div>
            </div>
        </div>
        

        <div class="xl:w-[50%] xl:h-[85%] xl:absolute xl:right-[182px] xl:-top-10 xl:-z-2 bg-hero  h-[85vh] w-[100%] mt-10 relative flex justify-center items-center">
            <div class="size-135 absolute">
                <img src="/nikeapp/images/{Shoe}" class="size-135" alt="">
            </div>
            <img src="/nikeapp/images/collection-background.svg" class="h-[85vh] w-[100%] object-cover" alt="">
            <div class="absolute min-w-[40rem] flex justify-between left-1/2  -translate-x-1/2 bottom-0 transform translate-y-1/2 gap-5">
                <button class="relative" onclick = {() => changeShoe('thumbnail-shoe1.svg')}>
                    <img src="/nikeapp/images/thumbnail-background.svg" class="size-45" alt="">
                    <div class="absolute translate-x-1 -translate-y-2/2 size-45">
                        <img src="/nikeapp/images/thumbnail-shoe1.svg" class="size-40" alt="">
                    </div>
                </button>
        
                <button class="relative" onclick = {() => changeShoe('thumbnail-shoe2.svg')}>
                    <img src="/nikeapp/images/thumbnail-background.svg" class="size-45" alt="">
                    <div class="absolute translate-x-1 -translate-y-2/2 size-45">
                        <img src="/nikeapp/images/thumbnail-shoe2.svg" class="size-40" alt="">
                    </div>
                </button>
        
                <button class="relative" onclick = {() => changeShoe('thumbnail-shoe3.svg')}>
                    <img src="/nikeapp/images/thumbnail-background.svg" class="size-45" alt="">
                    <div class="absolute translate-x-1 -translate-y-2/2 size-45">
                        <img src="/nikeapp/images/thumbnail-shoe3.svg" class="size-40" alt="">
                    </div>
                </button>
                
            </div>
        </div>
    </section> 
</div>


<div class="h-[25vh]"></div>
