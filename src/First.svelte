<script>
    export let firstColor = 'red'; 
	export let firstOpacity;
</script>

<style>
	.first {
        width: 100px;
		height: 100px;
		margin-bottom: 30px;
	}
</style>

<div style="background:{firstColor}; opacity:{firstOpacity}" class="first"></div>

<form action="#">
   <label>Укажите цвет фона: 
     <input on:change={event => firstColor = event.target.value} type="color" name="bg" value="#ffffff">
   </label>

   <label>Укажите видимость фона: 
     <input on:input={event => firstOpacity = event.target.value} type="range" name="op" min="0" max="1" step="0.1" value="1">
   </label>
</form>