<script>
export let progress = 0;

</script>



<div bp="grid">
 <div bp="offset-5@md 4@md 12@sm"
 class="progress-container">
 <div class="progress-bar" style="width: {progress}%;">
 <div class="sr-only">%{progress}</div>
 
 </div>
 </div>
</div>


<style>
.progress-container {
    margin: 20px 0;
    border: 1px solid rgb(194, 194, 194);
}

.progress-bar {
    height: 30px;
    background-color: rgb(77, 199, 55);
}

</style>