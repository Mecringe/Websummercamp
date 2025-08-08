<script>
    let { current, max, color} = $props();

</script>

<div class="border w-48 h-6">

<div 
        style="width: {(current / max) * 100}%"
    class="h-full  transition-all duration-1000 {color}"></div>

</div>
