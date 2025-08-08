<script>
    import Button from '../../componets/Button.svelte';
</script>
<div class="bg-green-500 w-screen">
<div class="prose p-5 ">

<h1 class="text-center">Jaeho's Profile</h1>

<hr/>


<div class="w-20 h-20 rounded-full bg-black overflow-hidden profile-image bg-cover bg-center hover:animate-spin">
</div>
<div>Jaeho Lee</div> 
<div>STATUS: Person</div>

<h2>About me</h2>
<p>Hi, my name is Jaeho.</p>

<h2>Componets</h2>

<Button text={'CLICK ME'} message={';)'} />
<Button text={'DONT CLICK ME'} message={';('} />

<h2>Haiku exercise</h2>


<div class= "backgroundcolorblue text-center">
<h3>Golden panko cloak </h3>
</div>
<div class= "backgroundcolorgreen text-center">
<h3>Tangy ton‑katsu sauce sighs</h3>
</div>
<div class= "backgroundcolorgray text-center">
<h3>Rice whispers comfort </h3>
</div>




</div>
</div>


<style>
    .profile-image {
        background-image: url("https://images.unsplash.com/photo-1540979129101-fef4ab23dbd6?q=80&w=2073&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D") ;
    }
    .backgroundcolorblue{
        background-color:rgb(111, 111, 255);
        animation: bounce 1s infinite;
    }
    .backgroundcolorgreen{
        background-color:rgb(213, 247, 162);
        animation: bounce 1s infinite;
    }
    .backgroundcolorgray{
        background-color: azure;
        animation: bounce 1s infinite;
 
    }
    .spin{
        animation: spin 1s infinite;
    }

</style>