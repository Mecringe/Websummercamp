<script>
    import { onMount } from"svelte";
	import Button from "../../componets/Button.svelte";
	import { passive } from "svelte/legacy";

    let point = $state(0);
    let clickp = $state(1);
    let pastiveIncome = $state(1);
    
    let upgradeclickcost = 5000000000
    let upgradepasivecost = -9999999999999999999999
    
    
    
    
    onMount(() => {
        //INTERVAl
        let pastiveTimer = setInterval(() => {
            point += pastiveIncome;

        }, 1000);

        return () => clearInterval(pastiveTimer);
    });

    function upgradeClickPower(amount) {
        if(point - amount *100 >= 0){
            point -= amount * 100;
            clickp +=amount;
        }
    }

    function increment() {
        point+= clickp;

    }
    function upgradepasiveincome(amount) {
        if(point - amount * 500 >=0) {
            point -=amount *500;
            pastiveIncome += amount;
        }
    }

    

</script>

<div class="h-screen bg-orange-800 flex flex-col justify-center items-center">
    <div class="flex flex-col items-start w-full">
    <div class="flex text-center border w-full"></div>
    <div>Sheckels {point}</div>
    <div class="flex text-center border w-full"></div>
    <div>Gear Power {clickp}</div>
    <div class="flex text-center border w-full"></div>
    <div>Pet Power {1 - pastiveIncome}</div>
    <div class="flex text-center border w-full"></div>
    </div>

    <button onclick={increment} class="hover:scale-120 active:scale-110 transition-all duration-100 h-48 w-35 rounded-full bg-gradient-to-b from-white to-blue-500"></button>
    <div class="flex text-center border w-full">
        <div class="flex flex-col w-1/2">
        <div>Gear Shop</div>
    <div class="flex text-center border w-full"></div>
        <Button text={"+1  $100"} fn={() => upgradeClickPower(1)}/>
        <Button text={"+5  $500"} fn={() => upgradeClickPower(5)}/>
        <Button text={"+10  $1,000"} fn={() => upgradeClickPower(10)}/>
        <Button text={"+100  $10,000"} fn={() => upgradeClickPower(100)}/>   
        </div>
        <div class="flex flex-col w-1/2">
        <div>Pet Shop</div>
    <div class="flex text-center border w-full"></div>
        <Button text={"+1 $500"} fn={() => upgradepasiveincome(1)}/>
        <Button text={"+10 $5,000"} fn={() => upgradepasiveincome(10)}/>
        <Button text={"+50 25,000"} fn={() => upgradepasiveincome(50)}/>
        <Button text={"+100 500,000"} fn={() => upgradepasiveincome(100)}/>


        
        </div>
        <div>
            <div class="flex text-center border w-full"></div>
    <h1>TRAVELING MERCHANT</h1>
    <div class="flex text-center border w-full"></div>
            <Button text={"Racoon -1 5,000,000,000"} fn={() => upgradeclickcost()}/>
            <Button text={"Racoon +2,000,000 9,999,999,999,999,999,999,999"} fn={() => upgradepasivecost()}/>
    </div>
    </div>
    

</div>
<style>
    :global(html) {
        scroll-behavior: smooth;
    }
</style>
