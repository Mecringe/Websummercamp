<script>
    let { text, fn } = $props();
        
    
</script>

<button
 onclick={fn}
  class="m-1 rounded border hover:scale-150 hover:animate-bounce active:blur-sm px-3 py-1 transition-all duration-200 hover:bg-black hover:text-white"
 >{text}</button>

