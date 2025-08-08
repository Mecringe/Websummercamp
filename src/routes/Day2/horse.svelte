<script>
    let {emote, position, color, animation} = $props();
</script>

<div class="flex items-center bg-orange-900 h-10">
    <div style="width:{position}%" class="shrink-0 h-full transition-all duration-1000 {color}"></div>
    <div class="animal hover:animation-spin bounce {animation}  bounce active:scale-200 transition-all  "> {emote}</div>
</div>

<style>
    .animal{
        font-size:60px;
    }
    .bounce{
        animation: bounce .5s infinite
    }
    .spin{
        animation: spin .5s linear infinite;
    }
</style>















































































































