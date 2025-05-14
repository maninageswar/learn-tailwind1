<script lang="ts">
    import ShoeCard from "$lib/components/ShoeCard.svelte";
    import ShippingCard from "$lib/components/ShippingCard.svelte";
    import { darkMode } from '../../../store.js';


    let Shoe = $state('big-shoe1.png');
    let darkMode1 = $state(false);
    function changeShoe(shoe:any) {
        Shoe = shoe;
    }

    function toggleDarkMode() {
        darkMode1 = !darkMode1
        // darkMode.update(() => darkMode1);
        document.documentElement.classList.toggle("dark")
    }
</script>


<div class="relative mx-20 flex justify-center ">
    <header class="absolute z-10 container mx-auto mt-5">
        
        <nav class="flex justify-between items-center">
            <img src="/nikeapp/images/header-logo.svg" class="cursor-pointer" alt="">
            <div class="hidden xl:flex gap-15 *:text-bookmark-grey text-xl *:cursor-pointer">
                <h2>Home</h2>
                <h2>About Us</h2>
                <h2>Products</h2>
                <h2>Contact Us</h2>
            </div>

            <div class="flex justify-end items-center">
                <h2 class="hidden [background-color: red] super xl:block text-xl xl:pr-5 cursor-pointer mr-4">Sign in / Explore now</h2>
                <!-- svelte-ignore a11y_consider_explicit_label -->
                <button class="xl:hidden">
                    <i class="text-2xl fa-solid fa-bars cursor-pointer"></i>
                </button>
                <div class="flex items-center mr-6">
                    <!-- <h2 class="mr-6 text-xl">dark mode</h2>
                    <label class="switch mr-5">
                        <input type="checkbox">
                        <span class="slider round"></span>
                    </label> -->
                    <button onclick={()=>{toggleDarkMode()}} class="switch">
                        <input bind:checked={darkMode1} id="checkbox" type="checkbox" />
                        <span class="slider">
                          <div class="star star_1"></div>
                          <div class="star star_2"></div>
                          <div class="star star_3"></div>
                          <svg viewBox="0 0 16 16" class="cloud_1 cloud">
                            <path
                              transform="matrix(.77976 0 0 .78395-299.99-418.63)"
                              fill="#fff"
                              d="m391.84 540.91c-.421-.329-.949-.524-1.523-.524-1.351 0-2.451 1.084-2.485 2.435-1.395.526-2.388 1.88-2.388 3.466 0 1.874 1.385 3.423 3.182 3.667v.034h12.73v-.006c1.775-.104 3.182-1.584 3.182-3.395 0-1.747-1.309-3.186-2.994-3.379.007-.106.011-.214.011-.322 0-2.707-2.271-4.901-5.072-4.901-2.073 0-3.856 1.202-4.643 2.925"
                            ></path>
                          </svg>
                        </span>
                      </button>
                </div>
            </div>
            
        </nav>
    </header>

    <section class="h-[100vh] w-[90vw] container mx-auto xl:flex xl:flex-row xl:justify-between sm:flex-col ">
        <div class="slidefromleft xl:w-[45%] xl:h-[100vh] sm:w-[100%] sm:h-[95vh] pt-[20vh]">
            <p class="text-nike-orange text-xl">Our Summer collections</p>
            <h1 class="mt-10 font-palanquin text-8xl font-[500] leading-[106px] xl:bg-white xl:mt-5 xl:w-[35vw] dark:text-white dark:bg-black">The New Arrival </h1>
            <br> 
            <h1 class="font-palanquin text-8xl font-[500] dark:text-white"><span class="text-nike-orange dark:text-nike-orange">Nike</span> Shoes</h1>
            
            <p class="text-xl text-bookmark-grey mt-8">Discover stylish Nike arrivals, quality <br>comfort, and innovation for your active life.</p>
            <button class="bg-nike-orange text-white mt-10 px-5 py-3 rounded-l-full rounded-r-full flex items-center">Shop Now <i class="ml-3 fa-solid fa-arrow-right"></i></button>
            <div class="flex justify-between mt-6 max-w-[25rem]">
                <div>
                    <h1 class="mt-10 font-palanquin text-5xl font-[500] dark:text-white">1k+</h1>
                    <p class="text-l text-bookmark-grey mt-2">Brands</p>
                </div>
                <div>
                    <h1 class="mt-10 font-palanquin text-5xl font-[500] dark:text-white">500+</h1>
                    <p class="text-l text-bookmark-grey mt-2">Shops</p>
                </div>
                <div>
                    <h1 class="mt-10 font-palanquin text-5xl font-[500] dark:text-white">250k+</h1>
                    <p class="text-l text-bookmark-grey mt-2">Customers</p>
                </div>
            </div>
        </div>
        <div class="relative xl:w-[55%] xl:h-[100vh] sm:w-[100%] sm:h-[85vh] xl:pt-[30vh] bg-[url(/nikeapp/images/collection-background.svg)] bg-cover bg-center flex justify-center items-end">
            <img class="3xl:top-1/2 3xl:left-1/2 3xl:-translate-x-1/2 3xl:-translate-y-1/2 slidefromright absolute w-[610px] h-[502px] translate-x-1 -translate-y-1/2 transform delay-120 duration-300 ease-in-out hover:scale-120" src="/nikeapp/images/{Shoe}" alt="">
            <div class="translate-y-1/2 flex justify-between gap-5 *:">
                <button class="rotatebutton bg-[url(/nikeapp/images/thumbnail-background.svg)] bg-cover bg-center size-45 flex justify-center items-center {Shoe == 'big-shoe1.png' ?'outline-2 outline-offset-2 rounded-xl outline-nike-orange' : ''}" onclick = {() => changeShoe('big-shoe1.png')}>
                    <img src="/nikeapp/images/thumbnail-shoe1.svg" class="size-40" alt="">
                </button>
                
                <button class="rotatebutton bg-[url(/nikeapp/images/thumbnail-background.svg)] bg-cover bg-center size-45 flex justify-center items-center {Shoe == 'big-shoe2.png' ?'outline-2 outline-offset-2 rounded-xl outline-nike-orange' : ''}" onclick = {() => changeShoe('big-shoe2.png')}>
                    <img src="/nikeapp/images/thumbnail-shoe2.svg" class="size-40" alt="">
                </button>

                <button class="rotatebutton bg-[url(/nikeapp/images/thumbnail-background.svg)] bg-cover bg-center size-45 flex justify-center items-center {Shoe == 'big-shoe3.png' ?'outline-2 outline-offset-2 rounded-xl outline-nike-orange' : ''}" onclick = {() => changeShoe('big-shoe3.png')}>
                    <img src="/nikeapp/images/thumbnail-shoe3.svg" class="size-40" alt="">
                </button>
            </div>
        </div>

        <div class="h-[25vh]"></div>
    </section>

</div>

<div class="mx-20">
    <section class="container mx-auto mt-55">
        <h1 class="text-[48px] font-[700] dark:text-white">Our <span class="text-nike-orange dark:nike-orange">Popular</span> Products</h1>
        <p class="text-bookmark-grey text-xl">Experience top-notch quality and style with our sought-after <br>selections. Discover a world of comfort, design, and value</p>
        <div class="mt-10 flex justify-between">
            <ShoeCard img="shoe4.svg" rating="4.5" shoeName="Nike Air Jordan-01" price="$200.20"></ShoeCard>
            <ShoeCard img="shoe5.svg" rating="4.5" shoeName="Nike Air Jordan-02" price="$210.20"></ShoeCard>
            <ShoeCard img="shoe6.svg" rating="4.5" shoeName="Nike Air Jordan-03" price="$220.20"></ShoeCard>
            <ShoeCard img="shoe7.svg" rating="4.5" shoeName="Nike Air Jordan-04" price="$230.20"></ShoeCard>
        </div>
    </section>
</div>

<div class="mx-20">
    <section class="container mx-auto mt-55 lg:flex lg:justify-between ">
        <div class="mt-10 lg:w-[40%] sm:w-[100%] flex flex-col">
            <h1 class="text-[48px] font-[700] dark:text-white">We Provide You <span class="text-nike-orange dark:text-nike-orange">Super Quality</span> Shoes</h1>
            <p class="text-bookmark-grey text-xl">Ensuring premium comfort and style, our meticulously crafted footwear is designed to elevate your experience, providing you with unmatched quality, innovation, and a touch of elegance.</p> <br>
            <p class="text-bookmark-grey text-xl">Our dedication to detail and excellence ensures your satisfaction.</p>
            <button class="bg-nike-orange text-white mt-10 px-5 py-3 w-[150px] rounded-l-full rounded-r-full flex items-center">View details</button>
        </div>
        <img src="/nikeapp/images/shoe8.svg" alt="">
    </section>
</div>

<div class="mx-20">
    <section class="container mx-auto mt-55 flex justify-between sm:flex-wrap">
        <ShippingCard img="truck-fast.svg" text="Free shipping" subtext="Enjoy seamless shopping with our complimentary shipping service."></ShippingCard>
        <ShippingCard img="shield-tick.svg" text="Secure Payment" subtext="Experience worry-free transactions with our secure payment options."></ShippingCard>
        <ShippingCard img="support.svg" text="Love to help you" subtext="Our dedicated team is here to assist you every step of the way."></ShippingCard>
    </section>
</div>

<div class="mx-20">
    <section class="container mx-auto mt-55 flex justify-between">
        <div class="mt-10 w-[40%] flex flex-col order-2 justify-center">
            <h1 class="text-[48px] font-[700] dark:text-white"><span class="text-nike-orange dark:text-nike-orange">Special</span> Offer</h1>
            <p class="text-bookmark-grey text-xl mt-5">Ensuring premium comfort and style, our meticulously crafted footwear is designed to elevate your experience, providing you with unmatched quality, innovation, and a touch of elegance.</p> <br>
            <p class="text-bookmark-grey text-xl">Our dedication to detail and excellence ensures your satisfaction.</p>
            <button class="bg-nike-orange text-white mt-10 px-5 py-3 w-[150px] rounded-l-full rounded-r-full flex items-center">View details</button>
        </div>
        <img src="/nikeapp/images/offer.svg" class="order-1" alt="">
    </section>
</div>


<style>
    /* @keyframes slidefromleft {
        from {
            transform: translateX(-50%);
        }
        to {
            transform: translateX(0);
        }
    }
    @keyframes slidefromright {
        from {
            transform: translateX(50%);
        }
        to {
            transform: translateX(0);
        }
    } */

    .slidefromleft {
        animation: var(--animate-slidefromleft1);
    }
    .slidefromright {
        animation: var(--animate-slidefromright1);
    } 

    @keyframes rotatebutton {
        from {
            rotate: 45deg;
        }

        to {
            rotate: 0deg;
        }

    }

    .rotatebutton {
        animation: rotatebutton 1s ease;
    }


    /* styles for toggle */
/* .switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
}

.switch input { 
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
  background-color: #2196F3;
}

input:focus + .slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
} */


/* From Uiverse.io by JustCode14 */ 
/* Theme Switch */
/* The switch - the box around the slider */
.switch {
  font-size: 17px;
  position: relative;
  display: inline-block;
  width: 4em;
  height: 2.2em;
  border-radius: 30px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #2a2a2a;
  transition: 0.4s;
  border-radius: 30px;
  overflow: hidden;
}

.slider:before {
  position: absolute;
  content: "";
  height: 1.2em;
  width: 1.2em;
  border-radius: 20px;
  left: 0.5em;
  bottom: 0.5em;
  transition: 0.4s;
  transition-timing-function: cubic-bezier(0.81, -0.04, 0.38, 1.5);
  box-shadow: inset 8px -4px 0px 0px #fff;
}

.switch input:checked + .slider {
  background-color: #00a6ff;
}

.switch input:checked + .slider:before {
  transform: translateX(1.8em);
  box-shadow: inset 15px -4px 0px 15px #ffcf48;
}

.star {
  background-color: #fff;
  border-radius: 50%;
  position: absolute;
  width: 5px;
  transition: all 0.4s;
  height: 5px;
}

.star_1 {
  left: 2.5em;
  top: 0.5em;
}

.star_2 {
  left: 2.2em;
  top: 1.2em;
}

.star_3 {
  left: 3em;
  top: 0.9em;
}

.switch input:checked ~ .slider .star {
  opacity: 0;
}

.cloud {
  width: 3.5em;
  position: absolute;
  bottom: -1.4em;
  left: -1.1em;
  opacity: 0;
  transition: all 0.4s;
}

.switch input:checked ~ .slider .cloud {
  opacity: 1;
}


</style>

