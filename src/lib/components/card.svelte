
<script lang="ts">
	let props = $props();
</script>

<div class="flex flex-col justify-between w-[15rem] h-[17rem] rounded-[10px] shadow-md p-5">
    <div class="flex flex-col items-center h-[10rem] justify-between">
        <img src="{props.img}" class="size-20" alt="chrome_image">
        <h5>{props.browser}</h5>
        <p class="text-bookmark-grey text-sm">{props.version}</p>
    </div>
    <button class="bg-bookmark-purple text-white mt-4 rounded-[5px] text-sm h-[2rem]">Add & Install Extension</button>
</div>