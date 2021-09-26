 <script>

	 import Goals from './practice.svelte'


let visible = false;
	 
	 
	 let name ='';
	 let age = Math.getRandomNumber;


	 function incrementAge(){
		age =Math.floor(Math.random() * 59 + 28);

	 }

	 function changeName(){
		 name = ""
	 }

	 function nameInput(event){
		 const enteredValue = event.target.enteredValue;
	 }
</script> 

<style>
	h1 {
		color: purple;
		text-align: center;
	}
	button {
  background-color: purple;
 border:teal;
  color: chocolate;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  font-family:monospace;
  align-content: center;
  
	}
  h3 {
   color:purple;
   align-items: center;
   text-align: center;
 
 }
 p{
   color: purple;
   font-size:xx-large;
  align-content: center;
  justify-content: center;
 
 }
.background{
	background-color:chocolate;
}

h2 {
   color: purple;
 
 }
</style>

<div class="background">
<h2> Do you want to know what age you will become a millionaire?  First, enter your name please!</h2>
<div>
	<input type="text" bind:value={name} placeholder="Type in your name"/>
</div>
<h3> Now click this button below to get results!</h3>
<button on:click="{incrementAge}"> Click To Find Age </button>
<h1>{name}, You'll become millionaire at age {age} !</h1>
{#if age > 56}
	<p>{name}. Push a little harder! Your hardwork will take much longer time.</p>
{:else if 40 > age}
	<p>{name}.Congratulations! You'll get rich at a young age.</p>   
{:else}
	<p>{name}. No worries! You'll get rich in average time.</p>
{/if}

</div>







<Goals /> 
