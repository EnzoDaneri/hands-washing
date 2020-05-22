<script>
 import Timer from './Timer.svelte'
 import HowTo from './HowTo.svelte'
 let audio;
 function timerEnds(e) {
     audio.play();
 }

</script>


<h1>Handwashing App</h1>
<Timer on:end={timerEnds}/> 

<HowTo/>

<h3>
<a href="https://www.who.int/gpsc/media/how_to_handwash_lge.gif">Fuente de imágen</a>
<a href="https://freesound.org/people/metrostock99/sounds/345086/#">Fuente del sonido</a>
</h3>

<audio bind:this={audio}
src="sound.wav"></audio>


<style>
 h1, h3 {
     text-align: center;
 }

</style>