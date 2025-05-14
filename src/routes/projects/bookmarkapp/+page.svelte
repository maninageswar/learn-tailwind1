<script>
    import Card from "$lib/components/card.svelte";
    let sideBar = $state(false)

    function toggleSideBar() {
        sideBar = !sideBar
    }
</script>

    <div class="relative">
    <!-- header -->
    <header class="container mx-auto  py-6">
        <nav class="flex justify-between items-center mx-5">
            <img src="/imgs/logo-bookmark.svg" alt="">
            <div class="sm:flex gap-x-10 items-baseline ml-2 text-bookmark-blue text-xs *:hover:cursor-pointer hidden">
                <h2>FEATURES</h2>
                <h2>PRICING</h2>
                <h2>CONTACT</h2>
                <button class="bg-bookmark-red text-bookmark-white w-[7rem] h-[2rem] rounded-[5px]">LOGIN</button>
            </div>
            <div class="sm:hidden">
                <button class="text-bookmark-blue hover:cursor-pointer" onclick={toggleSideBar}>
                    <i class="text-2xl fa-solid fa-bars"></i>
                </button>
            </div>
        </nav>
    </header>
    
     <section class="container mx-auto mt-20">
        <div class="mx-5">
            <div class="flex flex-col items-center md:flex-row md:justify-between">
                <img src="/imgs/hero-bg.png" alt="bookmark" class="w-[85%] md:w-[45%] relative md:order-last md:after:absolute md:after:w-25 md:after:h-25 md:after:border-2 md:after:z-10">
                <div class="md:order-first">
                    <h1 class="text-[min(4vw,100px)] text-center mt-8 md:text-start">A Simple Bookmark Manager</h1>
                    <p class="mt-4 text-bookmark-grey text-center md:text-start">A clean and simplw interfsce to organize your favourite websites. Open a new browser tab and see your sites load instantly. Try it for free.</p>
                    <div class="flex justify-center gap-3 mt-4 md:justify-start">
                        <button class="bg-bookmark-purple text-bookmark-white text-sm p-2 rounded-[5px]">Get it on Chrome</button>
                        <button class="bg-bookmark-white text-sm p-2 rounded-[5px] shadow-lg">Get it on Firefox</button>
                    </div>
                </div>
            </div>
            <div></div>
        </div>
     </section>

     <section class="container mx-auto mt-20 bg-bookmark-white">
        <div class="mx-auto max-w-[30rem] max-sm:max-w-[25rem]">
            <h1 class="text-[min(4vw,100px)] text-center mx-5">Features</h1>
            <p class="mt-4 text-bookmark-grey text-center mx-5">Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between your devices so you can access them on the go.</p>
        </div>
     </section>

     <section class="container mx-auto bg-bookmark-white">
        <div class="mx-5 pt-9">
            <div class="flex flex-col items-center md:flex-row md:justify-between">
                <img src="/imgs/illustration-features-tab-1.png" alt="bookmark" class="w-[85%] md:w-[45%] relative md:order-first md:after:absolute md:after:w-25 md:after:h-25 md:after:border-2 md:after:z-10">
                <div class="md:order-last md:ml-15">
                    <h1 class="text-[min(4vw,100px)] text-center mt-8 md:text-start">Bookmark in one click</h1>
                    <p class="mt-4 text-bookmark-grey text-center md:text-start">Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.</p>
                    <div class="flex justify-center gap-3 mt-4 md:justify-start">
                        <button class="bg-bookmark-purple text-bookmark-white text-sm p-2 rounded-[5px]">More info</button>
                    </div>
                </div>
            </div>
            <div></div>
        </div>
     </section>

     <section class="container mx-auto mt-20">
        <div class="mx-5">
            <div class="flex flex-col items-center md:flex-row md:justify-between">
                <img src="/imgs/illustration-features-tab-2.png" alt="bookmark" class="w-[85%] md:w-[45%] relative md:order-last md:after:absolute md:after:w-25 md:after:h-25 md:after:border-2 md:after:z-10">
                <div class="md:order-first">
                    <h1 class="text-[min(4vw,100px)] text-center mt-8 md:text-start">Intelligent search</h1>
                    <p class="mt-4 text-bookmark-grey text-center md:text-start">Our powerful search feature will help you find saved sites in no time at all. No need to crawl through all of your bookmarks.</p>
                    <div class="flex justify-center gap-3 mt-4 md:justify-start">
                        <button class="bg-bookmark-purple text-bookmark-white text-sm p-2 rounded-[5px]">More info</button>
                    </div>
                </div>
            </div>
            <div></div>
        </div>
     </section>

     <section class="container mx-auto bg-bookmark-white mt-5">
        <div class="mx-5 pt-4">
            <div class="flex flex-col items-center md:flex-row md:justify-between">
                <img src="/imgs/illustration-features-tab-3.png" alt="bookmark" class="w-[85%] md:w-[45%] relative md:order-first md:after:absolute md:after:w-25 md:after:h-25 md:after:border-2 md:after:z-10">
                <div class="md:order-last md:ml-15">
                    <h1 class="text-[min(4vw,100px)] text-center mt-8 md:text-start">Share your bookmarks</h1>
                    <p class="mt-4 text-bookmark-grey text-center md:text-start">Easily share your bookmarks and collections with others. Create a shareable link that you can send at the click of a button.</p>
                    <div class="flex justify-center gap-3 mt-4 md:justify-start">
                        <button class="bg-bookmark-purple text-bookmark-white text-sm p-2 rounded-[5px]">More info</button>
                    </div>
                </div>
            </div>
            <div></div>
        </div>
     </section>

     <section class="container mx-auto mt-20">
        <div class="mx-auto max-w-[30rem] max-sm:max-w-[25rem]">
            <h1 class="text-[min(3vw,4vw)] text-center mx-5">Download the extension</h1>
            <p class="mt-4 text-bookmark-grey text-center mx-5">We’ve got more browsers in the pipeline. Please do let us know if you’ve got a favourite you’d like us to prioritize.</p>
        </div>
     </section>

     <section class="container mx-auto mt-10 flex flex-wrap justify-evenly gap-5">
        <Card img="/imgs/logo-chrome.svg" browser = "Add to Chrome" version = "Minimum version 62"/>
        <Card img="/imgs/logo-firefox.svg" browser = "Add to Chrome" version = "Minimum version 62"/>
        <Card img="/imgs/logo-opera.svg" browser = "Add to Chrome" version = "Minimum version 62"/>
        <Card img="/imgs/logo-opera.svg" browser = "Add to Chrome" version = "Minimum version 62"/>
     </section>

     <section class="container mx-auto mt-10 bg-bookmark-white">
        <div class="mx-auto w-[40rem] max-sm:w-[25rem] p-8">
            <h1 class="text-[min(3vw,4vw)] text-center mx-5">Frequently Asked Questions</h1>
            <p class="mt-4 text-bookmark-grey text-center text-xs mx-5">Here are some of our FAQs. If you have any other questions you’d like answered please feel free to email us.</p>
            <div class="flex justify-between items-center mt-2">
                <h3>What is Bookmark?</h3>
                <img src="/imgs/icon-arrow.svg" class="size-2" alt="">
            </div>
            <hr class="border-t border-gray-200 mt-2">

            <div class="flex justify-between items-center mt-2">
                <h3>How can I request a new browser?</h3>
                <img src="/imgs/icon-arrow.svg" class="size-2" alt="">
            </div>
            <hr class="border-t border-gray-200 mt-2">

            <div class="flex justify-between items-center mt-2">
                <h3>Is there a mobile app?</h3>
                <img src="/imgs/icon-arrow.svg" class="size-2" alt="">
            </div>
            <hr class="border-t border-gray-200 mt-2">
            <div class="flex justify-between items-center mt-2">
                <h3>What about other Chromium browsers?</h3>
                <img src="/imgs/icon-arrow.svg" class="size-2" alt="">
            </div>
            <hr class="border-t border-gray-200 mt-2">
            
            <div class="mt-5 flex justify-center">
                <button class="bg-bookmark-purple text-bookmark-white text-sm p-2 rounded-[5px]">More info</button>
            </div>
        </div>
     </section>

    <div class="OpenSideBar flex flex-col gap-2 absolute w-[45vw] h-[100vh] z-10 top-0 right-[-45vw] bg-bookmark-white p-4 shadow-lg {sideBar ? 'visible' : 'hidden'}">
        <div class="flex justify-end pt-2 pr-1">
            <i class="text-2xl fa-solid fa-xmark" onclick={toggleSideBar}></i>
        </div>
        <h2>FEATURES</h2>
        <h2>PRICING</h2>
        <h2>CONTACT</h2>
        <h2>LOGIN</h2>
    </div>
    
    </div>

    <style>
        /* @keyframes animateOpenSideBar {
            from {
                transform: translateX(-45vw);
            }

            to {
                transform: translateX(0vw)
            }
        } */

        /* .OpenSideBar {
            animation: animateOpenSideBar 1s reverse backwards;
            transform: 0vm;
            animation: animateOpenSideBar 1s forwards;
            transform: translateX(-45vw);
        } */

        .OpenSideBar {
            transition-property: transform;
            transition-duration: 0.3s;
            transition-timing-function: ease-in-out;
        } 

        .visible {
            transform: translateX(-45vw);
        }
    </style>
     
