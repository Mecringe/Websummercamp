<script>
	import Horse from './horse.svelte';
	import Button from '../../componets/Button.svelte';

	let horses = $state([
		{
			emote: '🏇',
			position: 0,
			color: 'bg-gradient-to-r from-blue-400 to-white',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-gradient-to-r from-black to-blue-900',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-gradient-to-r from-red-400 to-white',

			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-gradient-to-r from-red-500 via-orange-400 to-yellow-500',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		},
		{
			emote: '🏇',
			position: 0,
			color: 'bg-blue-400',
			animation: 'bounce'
		}
	]);
	function progress() {
		let maxHorse = horses[0];
		for (let horse of horses) {
			let r = parseInt(Math.random() * 20);
			horse.position += r;
			if (horse.position > 100) {
				horse.position = 100;
			}

			if (horse.position > maxHorse.position) {
				maxHorse = horse;
			}
		}
	    for(let horse of horses) {
            if(horse.position == maxHorse.position) {
                horse.animation = 'spin';
            } else {
                horse.animation = 'bounce';
            }
        }
	}
    function reset() {
        for (let horse of horses) {
            horse.position = 0;
            // animation = horse.animation;
        }
    }
</script>

<div style="height: 600px;" class="bg-green-400">
	<div class="py-5 text-center text-2xl font-bold">HORSE RACING GAME</div>

	<Button text={'progress'} fn={progress} />
	<Button text={'RESET'} fn={reset} />
	<div class="py-10 pr-10">
		{#each horses as horse}
			<Horse
				emote={horse.emote}
				color={horse.color}
				animation={horse.animation}
				position={horse.position}
			/>
		{/each}
	</div>
</div>
