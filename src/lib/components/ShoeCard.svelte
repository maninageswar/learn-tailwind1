<script lang="ts">
    interface some {
        img:String
        rating:String,
        shoeName:String,
        price?:String
    }
	let props:some = $props();
</script>

<div class="flex flex-col">
    <img class="size-65" src="/nikeapp/images/{props.img}" alt="">
    <div class="mt-8">
        <p class="text-xl"><img class="inline mr-4 dark:text-white" src="/nikeapp/icons/star.svg" alt="">({props.rating})</p>
        <h3 class="text-2xl mt-3 font-[500] dark:text-white">{props.shoeName}</h3>
        <h3 class="text-2xl mt-2 font-[500] text-nike-orange">{props.price}</h3>
    </div>
</div>