<script>
  function hide(event) {
   const blocks = document.querySelectorAll('.block');
   if (event.target.classList.contains('block')) {
     event.target.classList.toggle('hide');
     [...blocks]
     .filter(item => item !== event.target)
     .map(item => item.classList.remove('hide'));
   }
  }
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

 .hide {
  opacity: 0;
 }
</style> 

<div class="wrap" on:click={hide}> 
 <div class="red block"></div>
 <div class="blue block"></div>
 <div class="green block"></div>
 <div class="hide"></div>
</div>