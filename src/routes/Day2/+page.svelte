<script>
    import Button from '../../componets/Button.svelte';
    import Loadingbar from '../../componets/Loadingbar.svelte';
    import Horserace from './Horserace.svelte';
    let progress = $state(10);

    function increment() {
        progress += 1;
        if (progress > 100) {
            progress =100
        }
    }

    function decrement() {
        progress -= 1;

        if (progress > 100) {
            progress =100
        }

    }
    function reset() {
        progress = 0;
    }
    function hi() {
        progress += 900000000;
    }
    
</script>







<div class="bg-red-500 hover:bg-blue-500 text-center transition-all duration-1000">
    Transition

</div>

<div class="hover:animate-spin bg-green-500 m-2 h-10 w-15 hover:bg-blue-900 border transition-all duration-1000">Box 1</div>
<div class="hover:animate-bounce hover:scale-900 m-2 h-10 w-15  border transition-all duration-1000">Box 2</div>
<div class="hover:blur-md m-2 h-10 w-15 bg-yellow-300 hover:invert border transition-all duration-1000">Box 3</div>
<div class="hover:brightness-200 hover:contrast-500 bg-blue-300 m-2 h-10 w-15  border transition-all duration-1000">Box 4</div>



<Button text={'Increment'}  fn={increment}/>
<Button text={'Decrement'}  fn={decrement}/>
<Button text={'RESET'}  fn={reset}/>
<Button text={'DONT PUSHHHHHHHHHHHHHH'}  fn={hi}/>



<Loadingbar color={"bg-blue-500"} current={progress} max={100}
/>


<Horserace/>







