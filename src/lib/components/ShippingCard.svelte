<script>
    let props = $props();
</script>

<div class="w-110 p-8 rounded-3xl shadow-2xl">
    <div class="rounded-full bg-nike-orange size-13 flex justify-center items-center mt-6">
        <img src="/nikeapp/icons/{props.img}" class="size20" alt="">
    </div>
    <h3 class="text-[28px] mt-5 dark:text-white">{props.text}</h3>
    <p class="mt-3 text-bookmark-grey text-lg">{props.subtext}</p>
</div>