<div class="bg-gradient-to-b from-black via-purple-900 to-black h-screen relative">
    <div class="absolute bg-yellow-200 w-10 h-10 left-1/2 top-1/2 -translate-1/2 rounded-full animate-pulse"></div>

        <!-- me-cury -->
    <div class="absolute w-15 h-15 left-1/2 top-1/2 -translate-1/2 rounded-full animate-[spin_5s_linear_infinite] border border-gray-200/40">
        <div class="absolute w-2 h-2 bg-blue-300 translate-0.5 rounded-full"></div>
    </div>

        <!-- pluto -->
    <div class="absolute w-30 h-30 left-1/2 top-1/2 -translate-1/2 rounded-full animate-[spin_20s_linear_infinite] border border-gray-200/40">
        <div class="absolute w-2 h-2 bg-blue-300 translate-0.5"></div>
    </div>
        <!-- earth -->
    <div class="absolute w-45 h-45 left-1/2 top-1/2 -translate-1/2 rounded-full animate-[spin_15s_linear_infinite] border border-gray-200/40">
        <div class="absolute w-2 h-2 bg-blue-300 translate-[10px] animate-[spin_15s_linear_infinite] " >
            <div class="absolute w-1 h-1 bg-white translate-[50px]  "> </div>
        </div>
            
    </div>
    
</div>


<!-- star -->
{#each Array(100) as _, i}
 <div class="rounded-full w-1 h-1 z-1 bg-white/60 absolute animate-pulse " 
 style="top:{Math.random() * 90}vh; left: {Math.random() * 90}vw;
 animation-delay: {Math.floor( Math.random() * 250)}ms;">
</div>
{/each}



<style>
    .centered {
        @apply absolute left-1/2 top-1/2 -translate-1/2;
    }
</style>