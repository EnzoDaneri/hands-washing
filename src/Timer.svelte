<script>
import ProgressBar from './ProgressBar.svelte'
const totalSeconds = 5;
let secondLeft = totalSeconds;
let isRunning = false;
$: progress = ( (totalSeconds - secondLeft) / totalSeconds) * 100;
function startTimer() {
 isRunning = true;   
 const timer = setInterval(() => {
  secondLeft -= 1;

if (secondLeft == 0) {
    clearInterval(timer);
    isRunning = false;
    secondLeft = totalSeconds
}
}, 1000);
}


</script>

<div bp="grid">
<h2 bp="offset-5@md 4@md 12@sm"
src="handwash.gif" alt="lavado de manos">Seconds Left:{secondLeft}</h2>
</div>
<ProgressBar progress={progress}/>

<div bp="grid">
<button disabled={isRunning} on:click={startTimer} class="start" bp="offset-5@md 4@md 12@sm"
>Start</button>

</div>

<style>
h2 {
    margin: 0;
}
.start {
    background-color: rgb(154, 73, 73);
    width: 100%;
    margin: 10px 0;
    height: 50px;

}

.start[disabled] {
    background-color:  rgb(194, 194, 194);
    cursor: not-allowed;
}
</style>