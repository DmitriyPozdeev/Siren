<script>

</script>

<style>
 .wrap {
     width: 640px;
     height: 100%;
 }
 .red {
    background: red;
    width: 50px;
    height: 50px;
    margin-bottom: 10px;
 }
 .blue {
    background: blue;
    width: 50px;
    height: 50px;
    margin-bottom: 10px;
 } 
 .green {
    background: green;
    width: 50px;
    height: 50px;
    margin-bottom: 10px;
 }

</style> 

<div class="wrap" on:click={event => event.target.style.visibility = 'hidden'}>
 <div class="red"></div>
 <div class="blue"></div>
 <div class="green"></div>
</div>