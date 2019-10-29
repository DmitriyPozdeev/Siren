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
 .block {
   display: inline-block;
   width: 100px;
   height: 100px;
   margin-right: 10px; 
 }
 .red {
    background: red;
 }
 .blue {
    background: blue;
 } 
 .green {
    background: green;
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